# ECO-TF-GCP-006: Right-size Cloud SQL machine types and storage

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Oversized instances and storage waste cost; small tweaks save a lot.

## Detection
Detect large `tier` or `disk_size` without clear need; very low CPU/IO metrics may hint at overprovisioning (heuristic).

## Remediation
Use monitoring to right-size tier and disk; enable autosizing where supported.

## KPI
- **Metric:** cloudsql_monthly_usd  
- **Estimated savings:** −10–40% DB cost

## GoalOps Template
- **Goal:** Right-size Cloud SQL machine types and storage  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Use monitoring to right-size tier and disk; enable autosizing where supported.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cloudsql_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

