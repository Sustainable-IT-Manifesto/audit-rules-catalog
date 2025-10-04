# ECO-REACT-007: List all dependencies in React useEffect

**Tech:** react  
**Severity:** medium  
**Category:** maintainability  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Missing deps create stale closures and inconsistent state.

## Detection
Detect `useEffect` with incomplete dependency arrays.

## Remediation
Provide all referenced variables/functions or justify with ESLint disable and memoization.

## KPI
- **Metric:** bug_rate  
- **Estimated savings:** Lower CFR

## GoalOps Template
- **Goal:** List all dependencies in React useEffect  
- **Reality:** Current implementation violates this rule.  
- **Options:** Provide all referenced variables/functions or justify with ESLint disable and memoization.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `bug_rate` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

