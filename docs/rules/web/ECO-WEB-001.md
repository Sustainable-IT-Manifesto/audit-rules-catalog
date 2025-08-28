# ECO-WEB-001: Bundle size budget exceeded

**Tech:** web  
**Severity:** high  
**Category:** quick_win  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Large bundles increase client energy and CDN egress.

## Detection
Detected bundle > budget (e.g., >250KB gzip).

## Recommendation
Code split, tree-shake, remove heavy libs, defer rarely used routes.

## KPI
- **Metric:** bundle_size_kb_gzip  
- **Estimated savings:** -20–60% bundle

## GoalOps Template
- **Goal:** Bundle size budget exceeded  
- **Reality:** Detected bundle > budget (e.g., >250KB gzip).  
- **Options:** Code split, tree-shake, remove heavy libs, defer rarely used routes.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `bundle_size_kb_gzip` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

