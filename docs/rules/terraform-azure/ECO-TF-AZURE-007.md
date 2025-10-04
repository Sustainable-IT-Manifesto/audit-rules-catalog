# ECO-TF-AZURE-007: Avoid overly permissive NSG rules (0.0.0.0/0)

**Tech:** terraform-azure  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Wide-open NSG rules increase attack surface and egress/ingress risk.

## Detection
Detect `azurerm_network_security_rule` allowing `source_address_prefix = "*"` or `0.0.0.0/0` for inbound; or broad ports ranges.

## Remediation
Restrict to necessary CIDRs/ports; use service tags and private endpoints where possible.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Avoid overly permissive NSG rules (0.0.0.0/0)  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Restrict to necessary CIDRs/ports; use service tags and private endpoints where possible.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

