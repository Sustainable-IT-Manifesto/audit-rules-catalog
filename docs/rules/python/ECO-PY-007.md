# ECO-PY-007: Avoid blocking calls in async functions

**Tech:** python  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Blocking operations inside `async def` prevent the event loop from making progress, hurting throughput and latency.

## Detection
AST: inside `ast.AsyncFunctionDef`, flag calls to known blocking APIs (e.g., `time.sleep`, `requests.*`, `subprocess.*`).

## Bad
```python
async def fetch_all(urls):
    for u in urls:
        requests.get(u)   # blocks
        time.sleep(1)     # blocks
```

## Good
```python
import asyncio, httpx

async def fetch_all(urls):
    async with httpx.AsyncClient() as client:
        for u in urls:
            await client.get(u)
            await asyncio.sleep(1)
```

## KPI
- **Metric:** latency_p95_ms  
- **Estimated savings:** 15–60% throughput increase

## GoalOps Template
- **Goal:** Avoid blocking calls in async functions  
- **Reality:** Blocking calls inside async functions (time.sleep, requests.*, subprocess.*) present in code paths.  
- **Options:** Apply recommended fix across hot/critical paths.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `latency_p95_ms` for improvement; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
