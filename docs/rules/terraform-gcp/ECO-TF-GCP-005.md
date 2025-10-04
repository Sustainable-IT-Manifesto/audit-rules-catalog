# ECO-TF-GCP-005: Enable Cloud SQL HA and automated backups

**Tech:** terraform-gcp  
**Severity:** high  
**Category:** reliability  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
HA and backups protect against zonal outages and data loss.

## Detection
Detect `google_sql_database_instance` missing `settings.backup_configuration.enabled` or not `settings.availability_type = "REGIONAL"`.

## Remediation
Enable automated backups and REGIONAL availability; test PITR where supported.

## KPI
- **Metric:** rto_rpo  
- **Estimated savings:** Lower RTO/RPO

## GoalOps Template
- **Goal:** Enable Cloud SQL HA and automated backups  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable automated backups and REGIONAL availability; test PITR where supported.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `rto_rpo` over a sprint.  
- **Three Ways Mapping:** Flow

---

