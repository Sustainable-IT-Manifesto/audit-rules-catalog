# ECO-TF-GCP-010: Use private GKE clusters and Shielded Nodes

**Tech:** terraform-gcp  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Private clusters minimize exposure; Shielded Nodes protect against rootkits/boot tampering.

## Detection
Detect `google_container_cluster` missing `private_cluster_config.enable_private_nodes = true` or `enable_shielded_nodes = true`.

## Remediation
Enable private nodes/endpoints and Shielded Nodes; restrict master authorized networks.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Use private GKE clusters and Shielded Nodes  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable private nodes/endpoints and Shielded Nodes; restrict master authorized networks.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

