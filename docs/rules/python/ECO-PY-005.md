# ECO-PY-005: Unbounded caching / memory growth

**Tech:** python  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Caches without bounds increase memory/GC and swap risk.

## Detection
lru_cache with no maxsize; dict caches never pruned.

## Recommendation
Set maxsize; periodic pruning; use TTL caches.

## KPI
- **Metric:** peak_rss_mb  
- **Estimated savings:** -10–30% RAM

## GoalOps Template
- **Goal:** Unbounded caching / memory growth  
- **Reality:** lru_cache with no maxsize; dict caches never pruned.  
- **Options:** Set maxsize; periodic pruning; use TTL caches.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `peak_rss_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

