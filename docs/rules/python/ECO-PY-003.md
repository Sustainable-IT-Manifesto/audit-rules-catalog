# ECO-PY-003: Inefficient JSON/CSV handling for large data

**Tech:** python  
**Severity:** medium  
**Category:** deep_work  
**Confidence:** 0.65  
**Tags:** Flow

---

## Rationale
Loading whole files into memory increases time/energy.

## Detection
json.load of large files; pandas without chunksize.

## Recommendation
Use streaming/chunked reads; ijson; pandas chunksize.

## KPI
- **Metric:** io_bytes  
- **Estimated savings:** -30–70% CPU/IO

## GoalOps Template
- **Goal:** Inefficient JSON/CSV handling for large data  
- **Reality:** json.load of large files; pandas without chunksize.  
- **Options:** Use streaming/chunked reads; ijson; pandas chunksize.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `io_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

