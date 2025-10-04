# ECO-TF-GCP-013: Optimize Cloud NAT configuration/cost

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Too many NATs or suboptimal min ports per VM wastes cost and IPs.

## Detection
Detect many `google_compute_router_nat` per VPC or missing auto-scaling config.

## Remediation
Consolidate NAT, tune min ports per VM, and prefer Private Google Access where possible.

## KPI
- **Metric:** nat_usd  
- **Estimated savings:** −10–40% NAT cost

## GoalOps Template
- **Goal:** Optimize Cloud NAT configuration/cost  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Consolidate NAT, tune min ports per VM, and prefer Private Google Access where possible.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `nat_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

