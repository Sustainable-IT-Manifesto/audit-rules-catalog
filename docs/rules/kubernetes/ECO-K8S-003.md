# ECO-K8S-003: Right-size log verbosity & retention

**Tech:** kubernetes  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Excessive logs increase I/O, storage, and costs.

## Detection
High log levels in production; long retention with no lifecycle.

## Recommendation
Reduce verbosity; add log rotation/retention policies.

## KPI
- **Metric:** log_bytes_per_day  
- **Estimated savings:** -30–70% logs

## GoalOps Template
- **Goal:** Right-size log verbosity & retention  
- **Reality:** High log levels in production; long retention with no lifecycle.  
- **Options:** Reduce verbosity; add log rotation/retention policies.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `log_bytes_per_day` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

