# ECO-TF-GCP-008: Use preemptible/Spot nodes for tolerant workloads

**Tech:** terraform-gcp  
**Severity:** high  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Preemptible/Spot nodes significantly cut cluster costs for suitable workloads.

## Detection
Detect node pools missing `preemptible = true` (or `spot = true`).

## Remediation
Add preemptible/Spot pools with PDBs and graceful disruption handling.

## KPI
- **Metric:** gke_monthly_usd  
- **Estimated savings:** −30–70% pool cost

## GoalOps Template
- **Goal:** Use preemptible/Spot nodes for tolerant workloads  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Add preemptible/Spot pools with PDBs and graceful disruption handling.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `gke_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

