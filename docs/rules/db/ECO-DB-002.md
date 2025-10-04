# ECO-DB-002: Avoid Cartesian joins (missing join predicates)

**Tech:** database  
**Severity:** high  
**Category:** performance  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Cross joins explode row counts and overwhelm compute and memory.

## Detection
Detect joins without predicates or with `1=1` conditions.

## Remediation
Add appropriate join conditions and indexes on join keys.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid Cartesian joins (missing join predicates)  
- **Reality:** Current implementation violates this rule.  
- **Options:** Add appropriate join conditions and indexes on join keys.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
