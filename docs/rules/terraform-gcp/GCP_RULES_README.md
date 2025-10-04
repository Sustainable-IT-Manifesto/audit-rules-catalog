# Terraform GCP Detector → Rule Mapping

Updated: 2025-10-04T12:33:17 UTC

| Detector Script | Rule ID | Title |
|---|---|---|
| `tf_gcp_logging_bucket_retention_missing.py` | `ECO-TF-GCP-001` | Set Cloud Logging bucket retention |
| `tf_gcp_gcs_lifecycle_missing.py` | `ECO-TF-GCP-002` | Add GCS lifecycle management |
| `tf_gcp_gcs_uniform_access_public_prevent.py` | `ECO-TF-GCP-003` | Enable Uniform Bucket-Level Access and Public Access Prevention |
| `tf_gcp_kms_key_rotation_period.py` | `ECO-TF-GCP-004` | Set Cloud KMS key rotation period |
| `tf_gcp_cloud_sql_ha_backups.py` | `ECO-TF-GCP-005` | Enable Cloud SQL HA and automated backups |
| `tf_gcp_cloud_sql_machine_rightsize.py` | `ECO-TF-GCP-006` | Right-size Cloud SQL machine types and storage |
| `tf_gcp_gke_autopilot_or_autoscaling_bounds.py` | `ECO-TF-GCP-007` | Use GKE Autopilot or set autoscaling bounds |
| `tf_gcp_gke_preemptible_spot_nodes.py` | `ECO-TF-GCP-008` | Use preemptible/Spot nodes for tolerant workloads |
| `tf_gcp_gke_workload_identity.py` | `ECO-TF-GCP-009` | Enable Workload Identity on GKE |
| `tf_gcp_gke_private_cluster_shielded.py` | `ECO-TF-GCP-010` | Use private GKE clusters and Shielded Nodes |
| `tf_gcp_vpc_flow_logs_on.py` | `ECO-TF-GCP-011` | Enable VPC Flow Logs on subnets |
| `tf_gcp_firewall_overly_permissive.py` | `ECO-TF-GCP-012` | Avoid overly permissive VPC firewall rules (0.0.0.0/0) |
| `tf_gcp_nat_gateway_cost.py` | `ECO-TF-GCP-013` | Optimize Cloud NAT configuration/cost |
| `tf_gcp_external_ip_unattached.py` | `ECO-TF-GCP-014` | Eliminate unattached external IPs |
| `tf_gcp_cloud_run_min_instances_zero.py` | `ECO-TF-GCP-015` | Set Cloud Run min instances to zero for spiky/idle services |
| `tf_gcp_bigquery_partition_cluster.py` | `ECO-TF-GCP-016` | Partition and cluster large BigQuery tables |

**Tech:** terraform-gcp
