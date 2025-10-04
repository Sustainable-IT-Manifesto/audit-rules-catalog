# ECO-TF-GCP-012: Avoid overly permissive VPC firewall rules (0.0.0.0/0)

**Tech:** terraform-gcp  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Wide-open rules increase attack surface.

## Detection
Detect `google_compute_firewall` allowing 0.0.0.0/0 ingress or broad port ranges.

## Remediation
Restrict CIDRs/ports; use service accounts and tags; prefer private access.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Avoid overly permissive VPC firewall rules (0.0.0.0/0)  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Restrict CIDRs/ports; use service accounts and tags; prefer private access.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

