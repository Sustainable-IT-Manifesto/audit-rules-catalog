# ECO-TF-005: Enable autoscaling on managed DBs and storage

**Tech:** terraform  
**Severity:** medium  
**Category:** deep_work  
**Confidence:** 0.65  
**Tags:** Flow

---

## Rationale
Static allocations keep headroom always-on.

## Detection
RDS/CloudSQL without autoscaling or storage autoscale.

## Recommendation
Turn on autoscaling; monitor floor/ceiling.

## KPI
- **Metric:** db_cpu_hours  
- **Estimated savings:** -15–40% CPU hrs

## GoalOps Template
- **Goal:** Enable autoscaling on managed DBs and storage  
- **Reality:** RDS/CloudSQL without autoscaling or storage autoscale.  
- **Options:** Turn on autoscaling; monitor floor/ceiling.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `db_cpu_hours` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

