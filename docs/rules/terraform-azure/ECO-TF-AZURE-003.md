# ECO-TF-AZURE-003: Add Azure Storage lifecycle management

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Tiering cold data to Cool/Archive and expiring stale blobs reduces storage spend.

## Detection
Detect `azurerm_storage_account` without `lifecycle_rule` in `azurerm_storage_management_policy`.

## Remediation
Create `azurerm_storage_management_policy` rules to transition/expire blobs based on last modified/last accessed time.

## KPI
- **Metric:** storage_usd  
- **Estimated savings:** −15–60% storage cost

## GoalOps Template
- **Goal:** Add Azure Storage lifecycle management  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Create `azurerm_storage_management_policy` rules to transition/expire blobs based on last modified/last accessed time.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `storage_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

