# ECO-TF-004: Shorten log retention for CloudWatch/AKS/GKE logs

**Tech:** terraform  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Long retention multiplies storage footprint.

## Detection
Retention set to default (indefinite).

## Recommendation
Set retention to 7–30d per compliance; export cold logs to glacier.

## KPI
- **Metric:** log_gb_month  
- **Estimated savings:** -20–60% log GB

## GoalOps Template
- **Goal:** Shorten log retention for CloudWatch/AKS/GKE logs  
- **Reality:** Retention set to default (indefinite).  
- **Options:** Set retention to 7–30d per compliance; export cold logs to glacier.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `log_gb_month` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

