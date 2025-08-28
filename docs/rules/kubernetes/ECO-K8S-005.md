# ECO-K8S-005: Evict unused initContainers and probes tuned

**Tech:** kubernetes  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.55  
**Tags:** Feedback

---

## Rationale
Overly aggressive probes waste CPU/IO; unused initContainers add time.

## Detection
Very short probe intervals/timeouts; initContainers doing one-off tasks repeatedly.

## Recommendation
Tune probes; remove redundant initContainers.

## KPI
- **Metric:** probe_cpu_seconds  
- **Estimated savings:** -10–25% CPU

## GoalOps Template
- **Goal:** Evict unused initContainers and probes tuned  
- **Reality:** Very short probe intervals/timeouts; initContainers doing one-off tasks repeatedly.  
- **Options:** Tune probes; remove redundant initContainers.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `probe_cpu_seconds` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Feedback

---

