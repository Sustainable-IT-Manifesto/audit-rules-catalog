# Terraform AWS Detector → Rule Mapping

Updated: 2025-10-04T12:28:07 UTC

| Detector Script | Rule ID | Title |
|---|---|---|
| `tf_aws_cost_asg_no_mixed_instances_spot.py` | `ECO-TF-AWS-001` | Leverage Spot with Mixed Instances for ASG |
| `tf_aws_cost_cloudwatch_logs_retention_missing.py` | `ECO-TF-AWS-002` | Set CloudWatch Logs retention |
| `tf_aws_cost_ebs_use_gp3.py` | `ECO-TF-AWS-003` | Prefer EBS gp3 over gp2 |
| `tf_aws_cost_ec2_large_instance_no_asg_or_spot.py` | `ECO-TF-AWS-004` | Avoid large single EC2 instances without ASG/Spot |
| `tf_aws_cost_eip_unattached.py` | `ECO-TF-AWS-005` | Eliminate unattached Elastic IPs |
| `tf_aws_cost_eks_nodegroups_autoscaling_bounds.py` | `ECO-TF-AWS-006` | Set EKS node group min/max bounds |
| `tf_aws_cost_elasticache_large_node.py` | `ECO-TF-AWS-007` | Right-size ElastiCache node types |
| `tf_aws_cost_nat_gateway_count.py` | `ECO-TF-AWS-008` | Minimize NAT Gateway count |
| `tf_aws_cost_rds_storage_type_and_autoscale.py` | `ECO-TF-AWS-009` | Cost anti-pattern in AWS Terraform |
| `tf_aws_cost_s3_lifecycle_missing.py` | `ECO-TF-AWS-010` | Cost anti-pattern in AWS Terraform |
| `tf_detect_db_missing_lifecycle_prevent_destroy.py` | `ECO-TF-AWS-011` | Cost anti-pattern in AWS Terraform |
| `tf_detect_ebs_unencrypted.py` | `ECO-TF-AWS-012` | Cost anti-pattern in AWS Terraform |
| `tf_detect_hardcoded_ami_or_region.py` | `ECO-TF-AWS-013` | Cost anti-pattern in AWS Terraform |
| `tf_detect_instance_uses_default_sg_or_subnet.py` | `ECO-TF-AWS-014` | Cost anti-pattern in AWS Terraform |
| `tf_detect_rds_publicly_accessible.py` | `ECO-TF-AWS-015` | Cost anti-pattern in AWS Terraform |
| `tf_detect_resource_without_tags.py` | `ECO-TF-AWS-016` | Cost anti-pattern in AWS Terraform |
| `tf_detect_s3_bucket_without_versioning_encryption.py` | `ECO-TF-AWS-017` | Cost anti-pattern in AWS Terraform |
| `tf_detect_sg_overly_permissive.py` | `ECO-TF-AWS-018` | Cost anti-pattern in AWS Terraform |

**Tech:** terraform-aws
