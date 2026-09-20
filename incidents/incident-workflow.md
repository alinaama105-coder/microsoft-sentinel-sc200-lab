# Microsoft Sentinel Incident Workflow

## Tier 1 SOC Exercise

I practised handling Microsoft Sentinel incidents using a structured investigation process.

### 1. Triage

- Review incident title and severity.
- Identify the analytics rule that generated the alert.
- Review affected entities and timestamps.
- Determine the scope of the activity.

### 2. Investigation

- Examine supporting Syslog events.
- Use KQL to investigate SSH authentication history.
- Review failed and successful authentication events.
- Identify relevant source-IP information.
- Compare the timeline with the detection logic.

### 3. Ownership

Incidents were assigned to myself during the lab to practise ownership of the investigation lifecycle.

### 4. Containment / Escalation

For the containment exercise, a suspicious external IP was identified and blocking was practised within the lab environment.

### 5. Documentation

Investigation notes recorded:

- What triggered the detection
- Events reviewed
- Timeline
- Relevant entities
- Findings
- Action taken
- Reason for closure or escalation

### 6. Closure

Incidents were closed only after documenting the investigation outcome.

## Example Closure Language

> Reviewed the authentication activity and supporting Syslog events. The event sequence, source information and related activity were assessed in the context of the lab scenario. Investigation findings and actions taken were documented before closure.

This wording is intentionally generic because each real incident requires evidence-based conclusions.
