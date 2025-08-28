# ECO-DOCKER-009: Use HEALTHCHECK wisely

**Tech:** docker  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.5  
**Tags:** Feedback

---

## Rationale
Missing healthchecks harm scheduling efficiency and autoscaling responses.

## Detection
No HEALTHCHECK in long-running services.

## Recommendation
Add lightweight HEALTHCHECK with sensible intervals/timeouts.

## KPI
- **Metric:** mean_time_to_recover  
- **Estimated savings:** -20–40% MTTR

## GoalOps Template
- **Goal:** Use HEALTHCHECK wisely  
- **Reality:** No HEALTHCHECK in long-running services.  
- **Options:** Add lightweight HEALTHCHECK with sensible intervals/timeouts.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `mean_time_to_recover` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Feedback

---

