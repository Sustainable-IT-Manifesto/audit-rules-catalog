# ECO-TF-002: Enable S3 lifecycle & intelligent tiering

**Tech:** terraform  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.75  
**Tags:** Flow

---

## Rationale
Cold data kept in standard tier wastes energy/cost.

## Detection
S3 buckets without lifecycle or tiering.

## Recommendation
Add lifecycle rules; enable intelligent tiering where access is unpredictable.

## KPI
- **Metric:** s3_standard_gb  
- **Estimated savings:** -30–80% std GB

## GoalOps Template
- **Goal:** Enable S3 lifecycle & intelligent tiering  
- **Reality:** S3 buckets without lifecycle or tiering.  
- **Options:** Add lifecycle rules; enable intelligent tiering where access is unpredictable.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `s3_standard_gb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

