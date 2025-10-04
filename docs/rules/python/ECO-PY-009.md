# ECO-PY-009: Use context manager for file operations

**Tech:** python  
**Severity:** low  
**Category:** style  
**Confidence:** 0.9  
**Tags:** Flow

---

## Rationale
Leaked file descriptors and unflushed buffers cause resource waste and intermittent failures.

## Detection
AST: `Call` to `open` not within `with` statement context.

## Bad
```python
f = open("data.txt", "w")
f.write("hello")
f.close()  # may be forgotten
```

## Good
```python
with open("data.txt", "w") as f:
    f.write("hello")
```

## KPI
- **Metric:** fd_leaks  
- **Estimated savings:** Lower resource leaks; fewer crashes

## GoalOps Template
- **Goal:** Use context manager for file operations  
- **Reality:** open() without context manager present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `fd_leaks` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
