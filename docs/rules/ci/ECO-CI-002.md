# ECO-CI-002: Missing dependency caching

**Tech:** ci  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.85  
**Tags:** Feedback

---

## Rationale
Cold builds fetch and build deps every run.

## Detection
No actions/cache or equivalent; lockfiles ignored.

## Recommendation
Add caching keyed by lockfile; cache Docker layers.

## KPI
- **Metric:** cache_hit_rate  
- **Estimated savings:** ≥85% hit rate

## GoalOps Template
- **Goal:** Missing dependency caching  
- **Reality:** No actions/cache or equivalent; lockfiles ignored.  
- **Options:** Add caching keyed by lockfile; cache Docker layers.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cache_hit_rate` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Feedback

---

