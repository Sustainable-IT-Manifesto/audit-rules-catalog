# ECO-DOCKERCOMPOSE-004: Set CPU/memory limits in compose

**Tech:** docker-compose  
**Severity:** high  
**Category:** resource_governance  
**Confidence:** 0.9  
**Tags:** Flow

---

## Rationale
No limits enable noisy-neighbor and overconsumption.

## Detection
Detect services missing 'deploy.resources.limits'.

## Remediation
Set conservative CPU/memory limits and requests.

## KPI
- **Metric:** host_cost_usd  
- **Estimated savings:** −5–20% cost

## GoalOps Template
- **Goal:** Set CPU/memory limits in compose  
- **Reality:** Current configuration violates this rule.  
- **Options:** Set conservative CPU/memory limits and requests.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `host_cost_usd` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

