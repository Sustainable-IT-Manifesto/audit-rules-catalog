# ECO-TF-GCP-001: Set Cloud Logging bucket retention

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Unlimited retention in Cloud Logging buckets grows costs; right-sizing retention per data class controls spend while meeting compliance.

## Detection
Detect `google_logging_project_bucket_config` (or _location_) without `retention_days`, or left at default high values.

## Remediation
Specify `retention_days` per log class; add sinks to BigQuery or GCS for cheaper long-term storage when needed.

## KPI
- **Metric:** logging_gb  
- **Estimated savings:** −10–40% log cost

## GoalOps Template
- **Goal:** Set Cloud Logging bucket retention  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Specify `retention_days` per log class; add sinks to BigQuery or GCS for cheaper long-term storage when needed.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `logging_gb` over a sprint.  
- **Three Ways Mapping:** Flow

---

