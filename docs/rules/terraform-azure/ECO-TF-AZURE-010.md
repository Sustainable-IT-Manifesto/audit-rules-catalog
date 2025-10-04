# ECO-TF-AZURE-010: Right-size managed disk SKUs

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Using Premium SSD when Standard SSD/HDD suffice drives unnecessary spend.

## Detection
Detect `azurerm_managed_disk` with `storage_account_type = "Premium_*"` on non-latency-critical volumes.

## Remediation
Prefer `StandardSSD_LRS` for general purpose; benchmark before using Premium.

## KPI
- **Metric:** disk_monthly_usd  
- **Estimated savings:** −10–50% disk cost

## GoalOps Template
- **Goal:** Right-size managed disk SKUs  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Prefer `StandardSSD_LRS` for general purpose; benchmark before using Premium.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `disk_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

