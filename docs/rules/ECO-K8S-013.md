# ECO-K8S-013: Avoid host namespaces and hostPath mounts

**Tech:** kubernetes  
**Severity:** high  
**Category:** security  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Host access allows node escape/lateral movement.

_Aligned with Kubernetes Pod Security Standards (**restricted** level**)_

## Detection
Detect `hostNetwork/hostPID/hostIPC: true` or `hostPath` volumes.

## Remediation
Disable host namespaces; use CSI/emptyDir/projected volumes.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Avoid host namespaces and hostPath mounts  
- **Reality:** Current manifests don’t comply.  
- **Options:** Disable host namespaces; use CSI/emptyDir/projected volumes.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` over a sprint.  
- **Three Ways Mapping:** Flow

---
