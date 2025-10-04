# ECO-TF-AWS-008: Minimize NAT Gateway count

**Tech:** terraform-aws  
**Severity:** high  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
NAT Gateways bill hourly + data; many are over-provisioned.

## Detection
Count `aws_nat_gateway` per VPC; detect > necessary.

## Remediation
Consolidate NAT where suitable; prefer VPC endpoints/private links.

## KPI
- **Metric:** nat_gw_usd  
- **Estimated savings:** −20–60% NAT cost

## GoalOps Template
- **Goal:** Minimize NAT Gateway count  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Consolidate NAT where suitable; prefer VPC endpoints/private links.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `nat_gw_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

