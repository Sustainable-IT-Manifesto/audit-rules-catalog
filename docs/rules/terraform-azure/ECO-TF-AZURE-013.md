# ECO-TF-AZURE-013: Use Spot node pools for AKS where suitable

**Tech:** terraform-azure  
**Severity:** high  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Spot nodes cut costs for tolerant workloads in AKS.

## Detection
Detect `azurerm_kubernetes_cluster_node_pool` without `priority = "Spot"`.

## Remediation
Add Spot node pools with taints/tolerations and Pod Disruption Budgets.

## KPI
- **Metric:** aks_monthly_usd  
- **Estimated savings:** −30–70% pool cost

## GoalOps Template
- **Goal:** Use Spot node pools for AKS where suitable  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Add Spot node pools with taints/tolerations and Pod Disruption Budgets.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `aks_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

