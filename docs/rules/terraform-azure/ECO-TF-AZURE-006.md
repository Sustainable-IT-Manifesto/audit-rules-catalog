# ECO-TF-AZURE-006: Enable Key Vault soft delete and purge protection

**Tech:** terraform-azure  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Accidental or malicious deletion of secrets/certs is catastrophic without soft delete and purge protection.

## Detection
Detect `azurerm_key_vault` missing `soft_delete_enabled = true` or `purge_protection_enabled = true`.

## Remediation
Set both `soft_delete_enabled = true` and `purge_protection_enabled = true`.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Enable Key Vault soft delete and purge protection  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set both `soft_delete_enabled = true` and `purge_protection_enabled = true`.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

