# ECO-PY-010: Avoid mutable default arguments

**Tech:** python  
**Severity:** low  
**Category:** bug_risk  
**Confidence:** 0.9  
**Tags:** Feedback

---

## Rationale
Defaults are evaluated once; shared mutable objects lead to surprising state sharing and perf anomalies.

## Detection
AST: `FunctionDef` defaults containing `List`, `Dict`, or `Set`.

## Bad
```python
def add(x, acc=[]):
    acc.append(x)
    return acc
```

## Good
```python
def add(x, acc=None):
    if acc is None:
        acc = []
    acc.append(x)
    return acc
```

## KPI
- **Metric:** bug_reports  
- **Estimated savings:** Stability and predictability

## GoalOps Template
- **Goal:** Avoid mutable default arguments  
- **Reality:** Mutable default arguments (list/dict/set) present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `bug_reports` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
