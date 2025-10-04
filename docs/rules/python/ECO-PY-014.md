# ECO-PY-014: Use logging instead of print in libraries

**Tech:** python  
**Severity:** low  
**Category:** style  
**Confidence:** 0.9  
**Tags:** Feedback

---

## Rationale
`print()` is unconfigurable noise for consumers; `logging` lets callers tune cost via levels/handlers.

## Detection
AST: `Call` to `print` outside `__main__`/CLI modules.

## Bad
```python
def do_work():
    print("debug:", expensive())  # always evaluates
```

## Good
```python
import logging
log = logging.getLogger(__name__)
def do_work():
    if log.isEnabledFor(logging.DEBUG):
        log.debug("debug: %s", expensive())
```

## KPI
- **Metric:** cpu_seconds  
- **Estimated savings:** 5–15% CPU in hot paths

## GoalOps Template
- **Goal:** Use logging instead of print in libraries  
- **Reality:** print() inside library code present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_seconds` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
