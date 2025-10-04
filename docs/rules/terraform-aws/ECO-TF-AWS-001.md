# ECO-TF-AWS-001: Leverage Spot with Mixed Instances for ASG

**Tech:** terraform-aws  
**Severity:** high  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Using only on‑demand instances in ASGs misses 30–70% savings potential.

## Detection
Find `aws_autoscaling_group` without `mixed_instances_policy`, or with `on_demand_percentage_above_base_capacity = 100`.

## Remediation
Adopt Mixed Instances Policy, set a balanced on‑demand percentage, and include multiple Spot instance types.

## KPI
- **Metric:** ec2_asg_usd  
- **Estimated savings:** −30–70% EC2 ASG cost

## GoalOps Template
- **Goal:** Leverage Spot with Mixed Instances for ASG  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Adopt Mixed Instances Policy, set a balanced on‑demand percentage, and include multiple Spot instance types.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ec2_asg_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

