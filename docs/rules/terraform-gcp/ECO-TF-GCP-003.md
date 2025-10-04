# ECO-TF-GCP-003: Enable Uniform Bucket-Level Access and Public Access Prevention

**Tech:** terraform-gcp  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
UBLA simplifies IAM and reduces ACL risk; Public Access Prevention blocks accidental exposure.

## Detection
Detect buckets missing `uniform_bucket_level_access = true` or `public_access_prevention = "enforced"`.

## Remediation
Enable both UBLA and Public Access Prevention on all buckets; grant access via IAM only.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Enable Uniform Bucket-Level Access and Public Access Prevention  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable both UBLA and Public Access Prevention on all buckets; grant access via IAM only.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

