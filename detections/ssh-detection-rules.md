# SSH Analytics Rule Exercises

## Objective

Turn KQL investigation logic into repeatable Microsoft Sentinel detections.

## Detection 1 - Repeated Failed SSH Authentication

The lab detection looked for repeated failed SSH activity.

Threshold used during the exercise:

- **3 or more failed attempts**
- **within 5 minutes**

The purpose was to identify authentication behaviour that warranted SOC review rather than treating every individual failed login as an incident.

## Detection 2 - Failure Followed by Success

A second exercise focused on the sequence:

```text
Repeated failed SSH attempts
            |
            v
Successful SSH authentication
```

This pattern was investigated because a successful authentication after repeated failures can warrant additional review.

## SOC Response

When a detection generated an incident, the workflow included:

1. Review alert details.
2. Examine the underlying authentication events.
3. Identify relevant source information/IP data.
4. Establish the timeline.
5. Check available context/watchlist information.
6. Document findings.
7. Decide whether containment or escalation was appropriate.
8. Record a closure reason and investigation notes.

These were controlled training exercises rather than production detections.
