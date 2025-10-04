# ECO-TF-AWS-002: Set CloudWatch Logs retention

**Tech:** terraform-aws  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Unlimited retention grows storage costs over time.

## Detection
Detect `aws_cloudwatch_log_group` without `retention_in_days`.

## Remediation
Set appropriate `retention_in_days` per log type/SLA.

## KPI
- **Metric:** cw_logs_gb  
- **Estimated savings:** −10–40% log storage

## GoalOps Template
- **Goal:** Set CloudWatch Logs retention  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set appropriate `retention_in_days` per log type/SLA.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cw_logs_gb`; time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

