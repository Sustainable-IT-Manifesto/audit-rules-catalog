# ECO-PY-013: Set timeouts for subprocess calls

**Tech:** python  
**Severity:** medium  
**Category:** resilience  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
External processes can hang and waste CPU/memory; timeouts cap impact and improve recovery.

## Detection
AST: calls to `subprocess.run/check_output/communicate` lacking `timeout=`.

## Bad
```python
import subprocess
subprocess.run(["convert", "in.png", "out.jpg"])
```

## Good
```python
import subprocess
subprocess.run(["convert", "in.png", "out.jpg"], timeout=30)
```

## KPI
- **Metric:** hung_processes  
- **Estimated savings:** Fewer zombie processes; bounded latency

## GoalOps Template
- **Goal:** Set timeouts for subprocess calls  
- **Reality:** subprocess.* without timeout present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `hung_processes` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
