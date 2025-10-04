# ECO-TF-AZURE-001: Configure Diagnostic Settings for platform logs

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Without Diagnostic Settings, Azure resources don't emit platform metrics/logs to Log Analytics/Storage/Event Hub, hurting observability and compliance.

## Detection
Detect resources lacking `azurerm_monitor_diagnostic_setting` binding to Log Analytics/Storage/Event Hub.

## Remediation
Create `azurerm_monitor_diagnostic_setting` for each critical resource and route relevant categories to Log Analytics with suitable retention.

## KPI
- **Metric:** observability_gaps  
- **Estimated savings:** Fewer gaps; faster MTTR

## GoalOps Template
- **Goal:** Configure Diagnostic Settings for platform logs  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Create `azurerm_monitor_diagnostic_setting` for each critical resource and route relevant categories to Log Analytics with suitable retention.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `observability_gaps` over a sprint.  
- **Three Ways Mapping:** Flow

---

