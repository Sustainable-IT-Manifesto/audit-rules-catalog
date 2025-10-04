# ECO-DOCKER-015: Use BuildKit cache mounts for package managers

**Tech:** docker  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Cache mounts avoid re-downloading packages across builds.

## Detection
Detect lack of 'RUN --mount=type=cache' for apt/pip/npm caches.

## Remediation
Adopt BuildKit and mount caches for package managers.

## KPI
- **Metric:** build_time_sec  
- **Estimated savings:** −15–40% time

## GoalOps Template
- **Goal:** Use BuildKit cache mounts for package managers  
- **Reality:** Current configuration violates this rule.  
- **Options:** Adopt BuildKit and mount caches for package managers.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `build_time_sec` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

