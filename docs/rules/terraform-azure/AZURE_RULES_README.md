# Terraform AZURE Detector → Rule Mapping

Updated: 2025-10-04T12:30:45 UTC

| Detector Script | Rule ID | Title |
|---|---|---|
| `tf_azure_aks_cluster_autoscaler_bounds.py` | `ECO-TF-AZURE-001` | Configure Diagnostic Settings for platform logs |
| `tf_azure_aks_node_pool_spot_missing.py` | `ECO-TF-AZURE-002` | Set Log Analytics workspace retention |
| `tf_azure_appsvc_http2_compression.py` | `ECO-TF-AZURE-003` | Add Azure Storage lifecycle management |
| `tf_azure_cosmos_autoscale_throughput.py` | `ECO-TF-AZURE-004` | Require secure transfer for Storage Accounts |
| `tf_azure_diagnostic_settings_missing.py` | `ECO-TF-AZURE-005` | Enable blob versioning and lifecycle for noncurrent versions |
| `tf_azure_kv_soft_delete_purge_protection_missing.py` | `ECO-TF-AZURE-006` | Enable Key Vault soft delete and purge protection |
| `tf_azure_log_analytics_retention_missing.py` | `ECO-TF-AZURE-007` | Avoid overly permissive NSG rules (0.0.0.0/0) |
| `tf_azure_managed_disk_type_cost.py` | `ECO-TF-AZURE-008` | Leverage Spot in Virtual Machine Scale Sets |
| `tf_azure_nsg_overly_permissive.py` | `ECO-TF-AZURE-009` | Set autoscale min/max bounds on VM Scale Sets |
| `tf_azure_public_ip_unattached.py` | `ECO-TF-AZURE-010` | Right-size managed disk SKUs |
| `tf_azure_sql_serverless_autopause.py` | `ECO-TF-AZURE-011` | Eliminate unattached Public IPs |
| `tf_azure_storage_lifecycle_missing.py` | `ECO-TF-AZURE-012` | Configure AKS cluster autoscaler with bounds |
| `tf_azure_storage_secure_transfer_disabled.py` | `ECO-TF-AZURE-013` | Use Spot node pools for AKS where suitable |
| `tf_azure_storage_versioning_missing.py` | `ECO-TF-AZURE-014` | Enable HTTP/2 and compression on App Service |
| `tf_azure_vmss_autoscale_bounds_missing.py` | `ECO-TF-AZURE-015` | Use Azure SQL Serverless with autopause where feasible |
| `tf_azure_vmss_spot_mixed_instances_missing.py` | `ECO-TF-AZURE-016` | Enable Cosmos DB autoscale throughput |

**Tech:** terraform-azure
