# ECO-DB-002: Excessive data retention without policy

**Tech:** database  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Old rows and blobs increase storage/backup energy.

## Detection
Tables without TTL/archival policy; ever-growing blobs.

## Recommendation
Add retention; tier cold data; purge safely.

## KPI
- **Metric:** storage_gb_month  
- **Estimated savings:** -20–60% GB

## GoalOps Template
- **Goal:** Excessive data retention without policy  
- **Reality:** Tables without TTL/archival policy; ever-growing blobs.  
- **Options:** Add retention; tier cold data; purge safely.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `storage_gb_month` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

