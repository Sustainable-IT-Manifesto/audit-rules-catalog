# ECO-WEB-003: Unused dependencies or polyfills

**Tech:** web  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Dead weight in node_modules inflates bundles and builds.

## Detection
Deps never imported; broad polyfills shipping to modern browsers.

## Recommendation
Prune deps; use targeted polyfills and browserslist.

## KPI
- **Metric:** bundle_modules_count  
- **Estimated savings:** -10–30% modules

## GoalOps Template
- **Goal:** Unused dependencies or polyfills  
- **Reality:** Deps never imported; broad polyfills shipping to modern browsers.  
- **Options:** Prune deps; use targeted polyfills and browserslist.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `bundle_modules_count` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

