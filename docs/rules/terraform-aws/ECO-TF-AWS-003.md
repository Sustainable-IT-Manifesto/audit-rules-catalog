# ECO-TF-AWS-003: Prefer EBS gp3 over gp2

**Tech:** terraform-aws  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
gp3 delivers similar/better performance at lower cost.

## Detection
Detect EBS volumes with `type = "gp2"`.

## Remediation
Migrate to `gp3`; size and provision IOPS/throughput as needed.

## KPI
- **Metric:** ebs_monthly_usd  
- **Estimated savings:** −10–20% EBS cost

## GoalOps Template
- **Goal:** Prefer EBS gp3 over gp2  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Migrate to `gp3`; size and provision IOPS/throughput as needed.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ebs_monthly_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

