# ECO-TF-003: Right-size instance types and autoscaling bounds

**Tech:** terraform  
**Severity:** high  
**Category:** deep_work  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Over-provisioned instances waste compute continuously.

## Detection
ASG min/max too high; large instance families with low CPU.

## Recommendation
Use utilization metrics to set min/max; try smaller/arm/spot where safe.

## KPI
- **Metric:** vCPU_hours  
- **Estimated savings:** -20–50% vCPU-hrs

## GoalOps Template
- **Goal:** Right-size instance types and autoscaling bounds  
- **Reality:** ASG min/max too high; large instance families with low CPU.  
- **Options:** Use utilization metrics to set min/max; try smaller/arm/spot where safe.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `vCPU_hours` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

