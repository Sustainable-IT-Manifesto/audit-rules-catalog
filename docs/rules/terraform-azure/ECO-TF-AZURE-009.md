# ECO-TF-AZURE-009: Set autoscale min/max bounds on VM Scale Sets

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Without bounds, scale sets may run too hot or cold, wasting resources or hurting SLOs.

## Detection
Detect `azurerm_monitor_autoscale_setting` missing or lacking sensible `minimum`, `maximum`.

## Remediation
Define `minimum`, `maximum`, and target metrics; add cool-down windows and reasonable step sizes.

## KPI
- **Metric:** vm_hours  
- **Estimated savings:** −10–40% VM hours

## GoalOps Template
- **Goal:** Set autoscale min/max bounds on VM Scale Sets  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Define `minimum`, `maximum`, and target metrics; add cool-down windows and reasonable step sizes.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `vm_hours` over a sprint.  
- **Three Ways Mapping:** Flow

---

