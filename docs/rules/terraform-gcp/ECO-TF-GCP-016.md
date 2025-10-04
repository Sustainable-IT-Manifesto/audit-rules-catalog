# ECO-TF-GCP-016: Partition and cluster large BigQuery tables

**Tech:** terraform-gcp  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Partitioning/clustering reduces scanned bytes and costs by pruning data.

## Detection
Detect `google_bigquery_table` without `time_partitioning`/`range_partitioning` and `clustering` on large tables.

## Remediation
Enable partitioning (ingestion/time/range) and cluster on common filter columns.

## KPI
- **Metric:** bq_scanned_bytes  
- **Estimated savings:** −30–90% scanned bytes

## GoalOps Template
- **Goal:** Partition and cluster large BigQuery tables  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable partitioning (ingestion/time/range) and cluster on common filter columns.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `bq_scanned_bytes` over a sprint.  
- **Three Ways Mapping:** Flow

---

