# ECO-DOCKER-006: Pin package versions for reproducible caching

**Tech:** docker  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.7  
**Tags:** Feedback

---

## Rationale
Unpinned deps cause cache busts and inconsistent sizes.

## Detection
Package managers without pinned versions in Dockerfile.

## Recommendation
Pin versions and use lockfiles; periodic controlled bumps.

## KPI
- **Metric:** cache_hit_rate  
- **Estimated savings:** ≥85% hit rate

## GoalOps Template
- **Goal:** Pin package versions for reproducible caching  
- **Reality:** Package managers without pinned versions in Dockerfile.  
- **Options:** Pin versions and use lockfiles; periodic controlled bumps.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cache_hit_rate` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Feedback

---

