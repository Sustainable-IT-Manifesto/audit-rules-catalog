# ECO-TF-AZURE-005: Enable blob versioning and lifecycle for noncurrent versions

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** reliability  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Versioning protects against deletes/overwrites; lifecycle controls cost of noncurrent versions.

## Detection
Detect `azurerm_storage_account` without `blob_properties.versioning_enabled = true` and no lifecycle for noncurrent versions.

## Remediation
Enable `versioning_enabled = true` and add lifecycle rules to expire older noncurrent versions.

## KPI
- **Metric:** recovery_time  
- **Estimated savings:** Lower MTTR; bounded storage

## GoalOps Template
- **Goal:** Enable blob versioning and lifecycle for noncurrent versions  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable `versioning_enabled = true` and add lifecycle rules to expire older noncurrent versions.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `recovery_time` over a sprint.  
- **Three Ways Mapping:** Flow

---

