# ECO-DOCKERCOMPOSE-009: Avoid publishing excessive ports

**Tech:** docker-compose  
**Severity:** low  
**Category:** security  
**Confidence:** 0.6  
**Tags:** Governance

---

## Rationale
Every exposed port increases attack surface and resource usage.

## Detection
Detect services with many published ports.

## Remediation
Publish only needed ports; use internal networks.

## KPI
- **Metric:** open_ports_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Avoid publishing excessive ports  
- **Reality:** Current configuration violates this rule.  
- **Options:** Publish only needed ports; use internal networks.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `open_ports_count` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

