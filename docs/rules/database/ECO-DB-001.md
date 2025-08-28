# ECO-DB-001: Indexes missing on hot queries

**Tech:** database  
**Severity:** high  
**Category:** deep_work  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Table scans increase CPU/IO and latency.

## Detection
Slow query patterns lacking supporting indexes.

## Recommendation
Add composite indexes; verify via EXPLAIN/ANALYZE.

## KPI
- **Metric:** cpu_seconds_per_query  
- **Estimated savings:** -30–90% CPU

## GoalOps Template
- **Goal:** Indexes missing on hot queries  
- **Reality:** Slow query patterns lacking supporting indexes.  
- **Options:** Add composite indexes; verify via EXPLAIN/ANALYZE.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_seconds_per_query` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

