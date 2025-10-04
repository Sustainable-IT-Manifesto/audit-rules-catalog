# ECO-TF-AZURE-002: Set Log Analytics workspace retention

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Unlimited retention inflates costs; right-sized retention controls spend while meeting compliance.

## Detection
Detect `azurerm_log_analytics_workspace` missing `retention_in_days` or set excessively high by default.

## Remediation
Set `retention_in_days` per data class (e.g., 30–180); use archive for long-term retention if required.

## KPI
- **Metric:** log_analytics_gb  
- **Estimated savings:** −10–40% log cost

## GoalOps Template
- **Goal:** Set Log Analytics workspace retention  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set `retention_in_days` per data class (e.g., 30–180); use archive for long-term retention if required.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `log_analytics_gb` over a sprint.  
- **Three Ways Mapping:** Flow

---

