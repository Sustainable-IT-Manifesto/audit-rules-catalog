# ECO-DB-003: Inefficient serialization (JSON blobs for hot paths)

**Tech:** database  
**Severity:** low  
**Category:** deep_work  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
JSON blobs force parse/scan vs structured columns.

## Detection
Frequent JSON_EXTRACT on hot path fields.

## Recommendation
Normalize columns or add generated columns with indexes.

## KPI
- **Metric:** cpu_seconds_per_query  
- **Estimated savings:** -10–40% CPU

## GoalOps Template
- **Goal:** Inefficient serialization (JSON blobs for hot paths)  
- **Reality:** Frequent JSON_EXTRACT on hot path fields.  
- **Options:** Normalize columns or add generated columns with indexes.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_seconds_per_query` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

