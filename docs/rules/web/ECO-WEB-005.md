# ECO-WEB-005: Excessive console/debug in production

**Tech:** web  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Console and verbose logging slow pages and leak info.

## Detection
console.debug/trace present in prod bundles.

## Recommendation
Strip logs during build; guard by env.

## KPI
- **Metric:** console_calls_per_page  
- **Estimated savings:** -80–100%

## GoalOps Template
- **Goal:** Excessive console/debug in production  
- **Reality:** console.debug/trace present in prod bundles.  
- **Options:** Strip logs during build; guard by env.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `console_calls_per_page` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

