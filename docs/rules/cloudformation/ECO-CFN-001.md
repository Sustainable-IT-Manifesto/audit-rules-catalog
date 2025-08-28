# ECO-CFN-001: Right-size Lambda memory & architecture

**Tech:** cloudformation  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.7  
**Tags:** Flow,Feedback

---

## Rationale
Over-allocating memory wastes cost/energy; x86 vs ARM choice matters.

## Detection
Functions with large memory and low duration; x86 where ARM viable.

## Recommendation
Tune memory to p95 latency; switch to ARM/Graviton if libs allow.

## KPI
- **Metric:** ms_per_invocation  
- **Estimated savings:** -10–40% ms

## GoalOps Template
- **Goal:** Right-size Lambda memory & architecture  
- **Reality:** Functions with large memory and low duration; x86 where ARM viable.  
- **Options:** Tune memory to p95 latency; switch to ARM/Graviton if libs allow.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ms_per_invocation` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow,Feedback

---

