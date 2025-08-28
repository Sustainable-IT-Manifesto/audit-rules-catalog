# ECO-CFN-002: Set S3 lifecycle transitions

**Tech:** cloudformation  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.75  
**Tags:** Flow

---

## Rationale
Default S3 retention uses standard tier by default.

## Detection
Buckets without LifecycleConfiguration.

## Recommendation
Add transitions to IA/Glacier; delete incomplete MPU after N days.

## KPI
- **Metric:** s3_standard_gb  
- **Estimated savings:** -30–80% std GB

## GoalOps Template
- **Goal:** Set S3 lifecycle transitions  
- **Reality:** Buckets without LifecycleConfiguration.  
- **Options:** Add transitions to IA/Glacier; delete incomplete MPU after N days.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `s3_standard_gb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

