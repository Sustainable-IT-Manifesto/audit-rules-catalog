# ECO-TF-AWS-006: Set EKS node group min/max bounds

**Tech:** terraform-aws  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Missing bounds leads to under/over-scaling and waste.

## Detection
Detect `aws_eks_node_group` missing `scaling_config.{min_size,max_size}`.

## Remediation
Define right min/max and target size per workload SLOs.

## KPI
- **Metric:** eks_node_hours  
- **Estimated savings:** −10–40% node hours

## GoalOps Template
- **Goal:** Set EKS node group min/max bounds  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Define right min/max and target size per workload SLOs.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `eks_node_hours`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

