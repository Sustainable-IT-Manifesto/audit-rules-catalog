# ECO-PY-011: Always set timeouts on network calls

**Tech:** python  
**Severity:** medium  
**Category:** resilience  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Lack of timeouts can stall threads and event loops, tie up connections, and inflate latency and cost.

## Detection
AST: `requests.*` calls with no `timeout=` kwarg.

## Bad
```python
import requests
requests.get(url)
```

## Good
```python
import requests
requests.get(url, timeout=5)
```

## KPI
- **Metric:** stuck_requests  
- **Estimated savings:** Reduced tail latency; fewer thread leaks

## GoalOps Template
- **Goal:** Always set timeouts on network calls  
- **Reality:** requests.* without timeout present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `stuck_requests` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
