# ECO-DOCKERCOMPOSE-012: Add HEALTHCHECK for long-running compose services

**Tech:** docker-compose  
**Severity:** medium  
**Category:** reliability  
**Confidence:** 0.7  
**Tags:** Feedback

---

## Rationale
Healthchecks improve self-healing and rollout safety.

## Detection
Detect services missing 'healthcheck:'.

## Remediation
Add a simple HTTP/TCP healthcheck with backoff.

## KPI
- **Metric:** mttr_minutes  
- **Estimated savings:** −10–30% MTTR

## GoalOps Template
- **Goal:** Add HEALTHCHECK for long-running compose services  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add a simple HTTP/TCP healthcheck with backoff.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `mttr_minutes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

