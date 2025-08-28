# ECO-DOCKER-005: Consolidate RUN layers & enable caching

**Tech:** docker  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Excess layers/cache misses enlarge images and slow builds.

## Detection
Many small RUN steps; apt/apk caches not cleaned; no --no-cache.

## Recommendation
Combine commands; use --no-cache; prune package caches.

## KPI
- **Metric:** build_time_sec  
- **Estimated savings:** -10–30% build time

## GoalOps Template
- **Goal:** Consolidate RUN layers & enable caching  
- **Reality:** Many small RUN steps; apt/apk caches not cleaned; no --no-cache.  
- **Options:** Combine commands; use --no-cache; prune package caches.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `build_time_sec` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

