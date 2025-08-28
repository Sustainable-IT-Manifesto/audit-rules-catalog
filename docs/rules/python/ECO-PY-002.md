# ECO-PY-002: N+1 DB query patterns

**Tech:** python  
**Severity:** high  
**Category:** deep_work  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Chatty ORM access explodes DB calls and CPU/IO.

## Detection
ORM calls in loops; missing select_related/prefetch_related.

## Recommendation
Batch queries; use joins; ORM eager loading.

## KPI
- **Metric:** db_queries_per_req  
- **Estimated savings:** -50–95% queries

## GoalOps Template
- **Goal:** N+1 DB query patterns  
- **Reality:** ORM calls in loops; missing select_related/prefetch_related.  
- **Options:** Batch queries; use joins; ORM eager loading.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `db_queries_per_req` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

