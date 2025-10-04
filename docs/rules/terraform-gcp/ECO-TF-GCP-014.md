# ECO-TF-GCP-014: Eliminate unattached external IPs

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Static external IPs incur charges when not in use.

## Detection
Detect `google_compute_address` not attached to instances/LBs.

## Remediation
Release unattached IPs; automate cleanup via inventory job.

## KPI
- **Metric:** external_ip_usd  
- **Estimated savings:** 100% of unattached IP cost

## GoalOps Template
- **Goal:** Eliminate unattached external IPs  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Release unattached IPs; automate cleanup via inventory job.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `external_ip_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

