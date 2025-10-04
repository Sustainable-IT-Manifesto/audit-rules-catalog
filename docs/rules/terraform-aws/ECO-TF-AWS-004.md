# ECO-TF-AWS-004: Avoid large single EC2 instances without ASG/Spot

**Tech:** terraform-aws  
**Severity:** high  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Single large instances are expensive and fragile.

## Detection
Detect `aws_instance` with large types and no ASG/Spot strategy.

## Remediation
Right-size; use ASG with mixed instances and Spot where appropriate.

## KPI
- **Metric:** ec2_monthly_usd  
- **Estimated savings:** −15–50% EC2 cost

## GoalOps Template
- **Goal:** Avoid large single EC2 instances without ASG/Spot  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Right-size; use ASG with mixed instances and Spot where appropriate.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ec2_monthly_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

