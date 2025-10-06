# ECO-K8S-024: Specify CPU/memory requests and limits

**Tech:** kubernetes  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Without resources, scheduling is suboptimal; contention and waste increase.

## Detection
Detect missing `resources.requests` and `resources.limits`.

## Remediation
Set sane requests/limits; consider VPA/HPA.

## KPI
- **Metric:** cpu_mem_waste  
- **Estimated savings:** −10–40% waste

## GoalOps Template
- **Goal:** Specify CPU/memory requests and limits  
- **Reality:** Current manifests don’t comply.  
- **Options:** Set sane requests/limits; consider VPA/HPA.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_mem_waste` over a sprint.  
- **Three Ways Mapping:** Flow

---
