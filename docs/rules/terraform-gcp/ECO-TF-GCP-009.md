# ECO-TF-GCP-009: Enable Workload Identity on GKE

**Tech:** terraform-gcp  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Workload Identity avoids node-wide service account keys and limits credential sprawl.

## Detection
Detect clusters missing `workload_identity_config`.

## Remediation
Enable Workload Identity and bind KSA↔GSA with least privilege.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Enable Workload Identity on GKE  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable Workload Identity and bind KSA↔GSA with least privilege.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

