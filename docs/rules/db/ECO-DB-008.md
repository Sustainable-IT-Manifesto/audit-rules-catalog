# ECO-DB-008: Use keyset (seek) pagination instead of OFFSET/LIMIT

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Large OFFSET values cause the DB to scan and discard many rows.

## Detection
Detect `OFFSET` pagination patterns.

## Remediation
Paginate with `WHERE id > last_seen_id ORDER BY id` (keyset/seek).

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Use keyset (seek) pagination instead of OFFSET/LIMIT  
- **Reality:** Current implementation violates this rule.  
- **Options:** Paginate with `WHERE id > last_seen_id ORDER BY id` (keyset/seek).  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
