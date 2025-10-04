# ECO-REACT-001: Avoid array index as React key

**Tech:** react  
**Severity:** low  
**Category:** maintainability  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Index keys break identity on reordering; causes extra re-renders.

## Detection
Detect `key={index}` patterns.

## Remediation
Use stable IDs for keys.

## KPI
- **Metric:** reconciliation_ms  
- **Estimated savings:** −10–40% time

## GoalOps Template
- **Goal:** Avoid array index as React key  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use stable IDs for keys.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `reconciliation_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

