# ECO-TF-AWS-007: Right-size ElastiCache node types

**Tech:** terraform-aws  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Oversized nodes waste memory/CPU and cash.

## Detection
Detect `aws_elasticache_cluster` with large `node_type`.

## Remediation
Profile hit/miss/latency; downsize or use cluster mode.

## KPI
- **Metric:** elasticache_usd  
- **Estimated savings:** −15–40% cache cost

## GoalOps Template
- **Goal:** Right-size ElastiCache node types  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Profile hit/miss/latency; downsize or use cluster mode.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `elasticache_usd`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

