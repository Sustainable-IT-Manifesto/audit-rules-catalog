# ECO-TF-AZURE-004: Require secure transfer for Storage Accounts

**Tech:** terraform-azure  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Disabling secure transfer allows plain HTTP; this risks data in transit.

## Detection
Detect `azurerm_storage_account` with `enable_https_traffic_only = false` or missing.

## Remediation
Set `enable_https_traffic_only = true` for all storage accounts.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Require secure transfer for Storage Accounts  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set `enable_https_traffic_only = true` for all storage accounts.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

