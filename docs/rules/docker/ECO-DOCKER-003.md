# ECO-DOCKER-003: .dockerignore is missing or too permissive

**Tech:** docker  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.9  
**Tags:** Flow,Feedback

---

## Rationale
Unnecessary build context increases build time and cache misses.

## Detection
No .dockerignore or missing patterns for node_modules/.venv/tests/docs/.git.

## Recommendation
Add .dockerignore with common excludes; confirm context reduction.

## KPI
- **Metric:** build_context_mb  
- **Estimated savings:** -50–95% context

## GoalOps Template
- **Goal:** .dockerignore is missing or too permissive  
- **Reality:** No .dockerignore or missing patterns for node_modules/.venv/tests/docs/.git.  
- **Options:** Add .dockerignore with common excludes; confirm context reduction.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `build_context_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow,Feedback

---

