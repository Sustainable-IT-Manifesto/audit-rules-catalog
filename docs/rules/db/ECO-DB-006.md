# ECO-DB-006: Avoid leading-wildcard LIKE patterns

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Patterns like `%term` prevent index usage and cause full scans.

## Detection
Detect `LIKE '%...'` where the wildcard starts the pattern.

## Remediation
Use suffix-only wildcards or full-text indexes; store search vectors.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid leading-wildcard LIKE patterns  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use suffix-only wildcards or full-text indexes; store search vectors.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
