# ECO-K8S-006: Node affinity/taints for efficient bin-packing

**Tech:** kubernetes  
**Severity:** medium  
**Category:** deep_work  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Poor bin-packing increases active nodes and cluster energy.

## Detection
No affinity/taints leading to spread across many nodes.

## Recommendation
Define affinity/anti-affinity to improve packing with SLOs.

## KPI
- **Metric:** node_hours  
- **Estimated savings:** -10–30% node-hours

## GoalOps Template
- **Goal:** Node affinity/taints for efficient bin-packing  
- **Reality:** No affinity/taints leading to spread across many nodes.  
- **Options:** Define affinity/anti-affinity to improve packing with SLOs.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `node_hours` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

