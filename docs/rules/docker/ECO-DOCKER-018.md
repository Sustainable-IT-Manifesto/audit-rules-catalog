# ECO-DOCKER-018: Pin base image by digest for reproducible builds

**Tech:** docker  
**Severity:** high  
**Category:** governance  
**Confidence:** 0.9  
**Tags:** Flow

---

## Rationale
Pinning the base image by **digest** (e.g., `@sha256:...`) guarantees the exact image bits are used on every build.
Tags can be moved or retagged, which leads to non-reproducible builds, cache misses, and unexpected security drift.

## Detection
Identify `FROM` lines that specify a tag (or even no tag) **without an image digest**, e.g.:
```
FROM python:3.12-slim           # missing @sha256:digest
```
A compliant example:
```
FROM python:3.12-slim@sha256:abc123...  # tag + digest
```

## Remediation
- Pin the base image to a specific digest, ideally alongside a stable tag (for readability).
- Keep a scheduled workflow to periodically bump digests after vulnerability scans.

## KPI
- **Metric:** change_failure_rate  
- **Estimated savings:** Lower CFR via reproducibility; fewer surprise drift incidents

## GoalOps Template
- **Goal:** Pin base images by digest  
- **Reality:** Current Dockerfile `FROM` lines are not pinned by digest.  
- **Options:** Add `@sha256:...` to base images; automate digest bumps with CI after scans.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `change_failure_rate` over one or more sprints.  
- **Three Ways Mapping:** Flow

---

