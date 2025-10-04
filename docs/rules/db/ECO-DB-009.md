# ECO-DB-009: Avoid SELECT * in queries

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Selecting all columns increases IO, CPU, and risk of schema-coupling; it also prevents covering indexes.

## Detection
Detect `SELECT *` patterns in SQL.

## Remediation
Enumerate only needed columns; keep result sets narrow.

## KPI
- **Metric:** io_bytes_read  
- **Estimated savings:** −5–25% IO

## GoalOps Template
- **Goal:** Avoid SELECT * in queries  
- **Reality:** Current implementation violates this rule.  
- **Options:** Enumerate only needed columns; keep result sets narrow.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `io_bytes_read` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
