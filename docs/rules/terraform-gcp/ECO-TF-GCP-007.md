# ECO-TF-GCP-007: Use GKE Autopilot or set autoscaling bounds

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Without bounds, clusters over/under-scale; Autopilot optimizes bin-packing.

## Detection
Detect `google_container_cluster` with cluster/node pool autoscaling disabled or missing sensible min/max; or not using `autopilot { enabled = true }`.

## Remediation
Enable Autopilot or define node pool autoscaling min/max per workload with cooldowns.

## KPI
- **Metric:** gke_node_hours  
- **Estimated savings:** −10–40% node hours

## GoalOps Template
- **Goal:** Use GKE Autopilot or set autoscaling bounds  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable Autopilot or define node pool autoscaling min/max per workload with cooldowns.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `gke_node_hours` over a sprint.  
- **Three Ways Mapping:** Flow

---

