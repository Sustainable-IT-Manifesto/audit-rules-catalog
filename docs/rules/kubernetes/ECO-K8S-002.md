# ECO-K8S-002: Enable Horizontal Pod Autoscaler (HPA)

**Tech:** kubernetes  
**Severity:** high  
**Category:** deep_work  
**Confidence:** 0.75  
**Tags:** Flow

---

## Rationale
Static replicas keep idle pods during low traffic.

## Detection
No HPA present for scalable services.

## Recommendation
Add HPA based on CPU/RPS/custom metrics; verify scale-to-zero where safe.

## KPI
- **Metric:** avg_replica_hours  
- **Estimated savings:** -20–60% replica-hours

## GoalOps Template
- **Goal:** Enable Horizontal Pod Autoscaler (HPA)  
- **Reality:** No HPA present for scalable services.  
- **Options:** Add HPA based on CPU/RPS/custom metrics; verify scale-to-zero where safe.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `avg_replica_hours` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

