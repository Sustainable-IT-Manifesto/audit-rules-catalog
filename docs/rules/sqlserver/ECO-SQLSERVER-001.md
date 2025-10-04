# ECO-SQLSERVER-001: Avoid ORDER BY RAND() for random sampling

**Tech:** sqlserver  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Sorting entire dataset by random value is O(N log N) and wastes resources.

## Detection
Detect `ORDER BY RAND()` / `RANDOM()` / `NEWID()` equivalents.

## Remediation
Use reservoir sampling, random primary key ranges, or precomputed random columns.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid ORDER BY RAND() for random sampling  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use reservoir sampling, random primary key ranges, or precomputed random columns.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
