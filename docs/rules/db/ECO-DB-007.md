# ECO-DB-007: Avoid NOT IN (SELECT ...) with NULL semantics

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
`NOT IN` with NULLs yields no rows; may force inefficient plans.

## Detection
Detect `NOT IN (SELECT ...)`.

## Remediation
Prefer `NOT EXISTS` with proper indexes.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid NOT IN (SELECT ...) with NULL semantics  
- **Reality:** Current implementation violates this rule.  
- **Options:** Prefer `NOT EXISTS` with proper indexes.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
