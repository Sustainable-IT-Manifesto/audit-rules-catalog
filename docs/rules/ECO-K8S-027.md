# ECO-K8S-027: Disallow privileged containers

**Tech:** kubernetes  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Privileged containers bypass isolation and can escalate to host control.

_Aligned with Kubernetes Pod Security Standards (**restricted** level**)_

## Detection
Detect `securityContext.privileged: true` in Pod/Container specs.

## Remediation
Set `privileged: false`; use minimal caps.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Disallow privileged containers  
- **Reality:** Current manifests don’t comply.  
- **Options:** Set `privileged: false`; use minimal caps.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---
