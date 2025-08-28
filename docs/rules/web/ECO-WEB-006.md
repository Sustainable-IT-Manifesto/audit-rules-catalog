# ECO-WEB-006: No HTTP caching headers / immutability

**Tech:** web  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.8  
**Tags:** Feedback

---

## Rationale
Lack of caching increases repeat transfer energy.

## Detection
Static assets served without long-lived cache headers.

## Recommendation
Add Cache-Control/ETag; content-hash filenames.

## KPI
- **Metric:** repeat_transfer_bytes  
- **Estimated savings:** -40–90%

## GoalOps Template
- **Goal:** No HTTP caching headers / immutability  
- **Reality:** Static assets served without long-lived cache headers.  
- **Options:** Add Cache-Control/ETag; content-hash filenames.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `repeat_transfer_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Feedback

---

