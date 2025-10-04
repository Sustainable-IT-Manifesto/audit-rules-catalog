# ECO-TF-GCP-015: Set Cloud Run min instances to zero for spiky/idle services

**Tech:** terraform-gcp  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Zero-min prevents idle compute burn; increase only for latency SLOs.

## Detection
Detect `google_cloud_run_service` with `min_instance_count > 0` without justification.

## Remediation
Use `min_instance_count = 0` for non-latency-critical services; cache warm if needed.

## KPI
- **Metric:** run_monthly_usd  
- **Estimated savings:** −5–30% service cost

## GoalOps Template
- **Goal:** Set Cloud Run min instances to zero for spiky/idle services  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Use `min_instance_count = 0` for non-latency-critical services; cache warm if needed.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `run_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

