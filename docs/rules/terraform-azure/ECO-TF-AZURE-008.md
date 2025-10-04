# ECO-TF-AZURE-008: Leverage Spot in Virtual Machine Scale Sets

**Tech:** terraform-azure  
**Severity:** high  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Spot VMs offer substantial savings for fault-tolerant workloads.

## Detection
Detect `azurerm_linux_virtual_machine_scale_set` / `azurerm_windows_virtual_machine_scale_set` without `priority = "Spot"`.

## Remediation
Use Spot with proper eviction policy (`Deallocate`) and buffer capacity; mix instance sizes in the scale set.

## KPI
- **Metric:** vm_monthly_usd  
- **Estimated savings:** −30–70% VM cost

## GoalOps Template
- **Goal:** Leverage Spot in Virtual Machine Scale Sets  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Use Spot with proper eviction policy (`Deallocate`) and buffer capacity; mix instance sizes in the scale set.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `vm_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

