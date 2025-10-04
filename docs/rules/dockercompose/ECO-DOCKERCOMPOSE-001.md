# ECO-DOCKERCOMPOSE-001: Do not mount the Docker socket inside containers

**Tech:** docker-compose  
**Severity:** high  
**Category:** security  
**Confidence:** 0.9  
**Tags:** Governance

---

## Rationale
Mounting /var/run/docker.sock grants root-equivalent host control.

## Detection
Detect volumes mapping docker.sock.

## Remediation
Avoid mounting docker.sock; use remote APIs or sidecars.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Do not mount the Docker socket inside containers  
- **Reality:** Current configuration violates this rule.  
- **Options:** Avoid mounting docker.sock; use remote APIs or sidecars.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

