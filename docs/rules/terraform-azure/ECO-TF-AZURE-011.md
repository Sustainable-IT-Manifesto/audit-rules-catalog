# ECO-TF-AZURE-011: Eliminate unattached Public IPs

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Unassociated Public IPs incur monthly charges.

## Detection
Detect `azurerm_public_ip` not referenced by NICs/LBs.

## Remediation
Release or associate unused Public IPs; automate cleanup.

## KPI
- **Metric:** public_ip_usd  
- **Estimated savings:** 100% of unattached IP cost

## GoalOps Template
- **Goal:** Eliminate unattached Public IPs  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Release or associate unused Public IPs; automate cleanup.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `public_ip_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

