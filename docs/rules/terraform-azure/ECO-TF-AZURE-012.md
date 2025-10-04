# ECO-TF-AZURE-012: Configure AKS cluster autoscaler with bounds

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Missing min/max bounds and scale-down delays can waste node hours.

## Detection
Detect `azurerm_kubernetes_cluster` where `auto_scaler_profile`/`default_node_pool` lack min/max or tuned delays.

## Remediation
Set reasonable min/max per node pool and `scale_down_delay_after_add`/`scale_down_unneeded`.

## KPI
- **Metric:** aks_node_hours  
- **Estimated savings:** −10–40% node hours

## GoalOps Template
- **Goal:** Configure AKS cluster autoscaler with bounds  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set reasonable min/max per node pool and `scale_down_delay_after_add`/`scale_down_unneeded`.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `aks_node_hours` over a sprint.  
- **Three Ways Mapping:** Flow

---

