# ECO-TF-GCP-004: Set Cloud KMS key rotation period

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Regular key rotation limits blast radius of compromised keys.

## Detection
Detect `google_kms_crypto_key` missing `rotation_period`.

## Remediation
Set `rotation_period` per policy (e.g., 30–90 days) and enable scheduled rotation.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Set Cloud KMS key rotation period  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set `rotation_period` per policy (e.g., 30–90 days) and enable scheduled rotation.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---

