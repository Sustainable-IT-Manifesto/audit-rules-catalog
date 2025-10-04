# ECO-TF-GCP-002: Add GCS lifecycle management

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Tiering and expiring stale blobs reduces storage spend.

## Detection
Detect `google_storage_bucket` without a `lifecycle_rule`.

## Remediation
Configure `lifecycle_rule` to transition cold objects and expire stale versions.

## KPI
- **Metric:** gcs_storage_usd  
- **Estimated savings:** −15–60% storage cost

## GoalOps Template
- **Goal:** Add GCS lifecycle management  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Configure `lifecycle_rule` to transition cold objects and expire stale versions.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `gcs_storage_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

