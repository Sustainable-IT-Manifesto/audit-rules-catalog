# ECO-PY-012: Use parameterized SQL, not string concatenation

**Tech:** python  
**Severity:** high  
**Category:** security_perf  
**Confidence:** 0.9  
**Tags:** Flow

---

## Rationale
String-building queries are unsafe (SQL injection) and disable database query plan caching.

## Detection
AST: `cursor.execute(...)` first arg is `BinOp(Add)` or `JoinedStr` (f-string).

## Bad
```python
cursor.execute(f"SELECT * FROM users WHERE id = {user_id}")
```

## Good
```python
cursor.execute("SELECT * FROM users WHERE id = %s", (user_id,))
```

## KPI
- **Metric:** db_cpu_ms  
- **Estimated savings:** Safer queries; better plan reuse

## GoalOps Template
- **Goal:** Use parameterized SQL, not string concatenation  
- **Reality:** String concatenation or f-strings in SQL execute present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `db_cpu_ms` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
