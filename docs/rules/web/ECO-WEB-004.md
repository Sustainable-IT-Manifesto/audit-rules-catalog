# ECO-WEB-004: Client polling where events/streams suffice

**Tech:** web  
**Severity:** medium  
**Category:** deep_work  
**Confidence:** 0.75  
**Tags:** Flow

---

## Rationale
Frequent polling wastes radio/CPU cycles.

## Detection
Intervals <30s for endpoints supporting SSE/webhooks.

## Recommendation
Switch to SSE/WebSockets/webhooks with backoff.

## KPI
- **Metric:** poll_requests_per_hour  
- **Estimated savings:** -50–95% requests

## GoalOps Template
- **Goal:** Client polling where events/streams suffice  
- **Reality:** Intervals <30s for endpoints supporting SSE/webhooks.  
- **Options:** Switch to SSE/WebSockets/webhooks with backoff.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `poll_requests_per_hour` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

