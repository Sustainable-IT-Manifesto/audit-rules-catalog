# ECO-TF-GCP-011: Enable VPC Flow Logs on subnets

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Flow logs aid troubleshooting, capacity planning, and security analytics.

## Detection
Detect `google_compute_subnetwork` with `enable_flow_logs = false` or missing.

## Remediation
Set `enable_flow_logs = true` with sensible sampling/aggregation.

## KPI
- **Metric:** observability_gaps  
- **Estimated savings:** Fewer gaps

## GoalOps Template
- **Goal:** Enable VPC Flow Logs on subnets  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set `enable_flow_logs = true` with sensible sampling/aggregation.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `observability_gaps` over a sprint.  
- **Three Ways Mapping:** Flow

---

