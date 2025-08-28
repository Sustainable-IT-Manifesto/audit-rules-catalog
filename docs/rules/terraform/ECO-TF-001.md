# ECO-TF-001: Use gp3 (or latest) over gp2 for EBS

**Tech:** terraform  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Modern volumes provide better perf per watt and lower cost.

## Detection
AWS EBS volumes on gp2.

## Recommendation
Switch to gp3 with tuned throughput/IOPS.

## KPI
- **Metric:** ebs_gb_month  
- **Estimated savings:** -10–20% cost/energy

## GoalOps Template
- **Goal:** Use gp3 (or latest) over gp2 for EBS  
- **Reality:** AWS EBS volumes on gp2.  
- **Options:** Switch to gp3 with tuned throughput/IOPS.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ebs_gb_month` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

