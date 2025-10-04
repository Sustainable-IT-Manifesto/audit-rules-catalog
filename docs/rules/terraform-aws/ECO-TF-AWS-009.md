# ECO-TF-AWS-009: Cost anti-pattern in AWS Terraform

**Tech:** terraform-aws  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
This configuration likely increases spend without clear benefit.

## Detection
Detector identifies the anti-pattern via HCL/regex.

## Remediation
Apply AWS best practices per FinOps & Well-Architected.

## KPI
- **Metric:** cloud_cost_usd  
- **Estimated savings:** Reduced cost

## GoalOps Template
- **Goal:** Cost anti-pattern in AWS Terraform  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Apply AWS best practices per FinOps & Well-Architected.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cloud_cost_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

