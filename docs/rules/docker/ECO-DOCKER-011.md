# ECO-DOCKER-011: Avoid :latest image tags; pin tag and digest

**Tech:** docker, docker-compose  
**Severity:** high  
**Category:** quick_win  
**Confidence:** 0.9  
**Tags:** Flow

---

## Rationale
Using ':latest' causes non-reproducible builds and cache misses.

## Detection
Detect FROM or image: lines referencing ':latest'.

## Remediation
Pin to a specific tag and digest (e.g., myimg:1.2@sha256:...).

## KPI
- **Metric:** image_pull_bytes  
- **Estimated savings:** −10–40% pulls

## GoalOps Template
- **Goal:** Avoid :latest image tags; pin tag and digest  
- **Reality:** Current configuration violates this rule.  
- **Options:** Pin to a specific tag and digest (e.g., myimg:1.2@sha256:...).  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_pull_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

