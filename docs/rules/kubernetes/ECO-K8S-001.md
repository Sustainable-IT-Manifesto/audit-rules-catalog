# ECO-K8S-001: Set CPU & memory requests/limits appropriately

**Tech:** kubernetes  
**Severity:** critical  
**Category:** quick_win  
**Confidence:** 0.85  
**Tags:** Flow,Feedback

---

## Rationale
Missing/misaligned requests/limits cause overcommit waste or throttling.

## Detection
Containers without resources or with requests >> observed usage.

## Recommendation
Set requests to p95 usage, limits ~1.5–2x; monitor and tune.

## KPI
- **Metric:** cpu_request_to_usage_ratio  
- **Estimated savings:** -20–50% CPU waste

## GoalOps Template
- **Goal:** Set CPU & memory requests/limits appropriately  
- **Reality:** Containers without resources or with requests >> observed usage.  
- **Options:** Set requests to p95 usage, limits ~1.5–2x; monitor and tune.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_request_to_usage_ratio` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow,Feedback

---

