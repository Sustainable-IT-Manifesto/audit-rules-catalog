# ECO-DB-004: Avoid functions on indexed columns in WHERE

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Wrapping columns in functions prevents index usage.

## Detection
Detect patterns like `WHERE LOWER(col) = 'x'` or `DATE(col) = ...`.

## Remediation
Normalize data at write time or use computed/functional indexes.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid functions on indexed columns in WHERE  
- **Reality:** Current implementation violates this rule.  
- **Options:** Normalize data at write time or use computed/functional indexes.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
