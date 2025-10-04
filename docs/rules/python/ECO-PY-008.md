# ECO-PY-008: Avoid bare or overly broad `except:`

**Tech:** python  
**Severity:** medium  
**Category:** correctness  
**Confidence:** 0.8  
**Tags:** Feedback

---

## Rationale
Catching everything hides bugs, prevents retries/backoff, and can mask high-cost error paths.

## Detection
AST: `ExceptHandler` with no type, or catching `Exception`/`BaseException` without re-raise/logging.

## Bad
```python
try:
    do_work()
except:
    pass
```

## Good
```python
try:
    do_work()
except (IOError, ValueError) as e:
    logger.warning("recoverable: %s", e)
    handle_recoverable(e)
```

## KPI
- **Metric:** error_rate  
- **Estimated savings:** Fewer masked failures; improved stability

## GoalOps Template
- **Goal:** Avoid bare or overly broad `except:`  
- **Reality:** Bare or overly broad exception handlers present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `error_rate` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
