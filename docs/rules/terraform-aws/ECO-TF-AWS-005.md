# ECO-TF-AWS-005: Eliminate unattached Elastic IPs

**Tech:** terraform-aws  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Unattached EIPs incur charges and management overhead.

## Detection
Detect `aws_eip` not associated to instances or ENIs.

## Remediation
Release unused EIPs; automate cleanup.

## KPI
- **Metric:** eip_monthly_usd  
- **Estimated savings:** 100% of unattached EIP cost

## GoalOps Template
- **Goal:** Eliminate unattached Elastic IPs  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Release unused EIPs; automate cleanup.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `eip_monthly_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

