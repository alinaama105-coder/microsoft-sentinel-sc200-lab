# Microsoft Sentinel SC-200 SOC Lab

A hands-on Microsoft security operations lab built to practise SIEM monitoring, KQL investigation, detection engineering, incident handling, threat intelligence/watchlists, containment and identity security.

## Project Overview

I built an Azure-based SOC lab while developing practical skills aligned with the Microsoft SC-200 Security Operations Analyst role.

The project progressed from Linux telemetry and SSH monitoring in Microsoft Sentinel to incident investigation and Microsoft Entra ID identity-security exercises.

## Lab Components

- Microsoft Azure
- Linux virtual machine
- Log Analytics workspace
- Microsoft Sentinel
- Syslog
- Kusto Query Language (KQL)
- Sentinel analytics rules
- Incidents
- Watchlists
- Microsoft Entra ID
- Sign-in logs
- Conditional Access

## Monitoring Workflow

```text
Linux VM
   |
   v
Syslog
   |
   v
Log Analytics
   |
   v
Microsoft Sentinel
   |
   +--> KQL investigation
   +--> Analytics rules
   +--> Incidents
   +--> Watchlist correlation
   |
   v
Triage / Investigation / Containment / Closure
```

## SSH Detection Work

I used KQL to investigate Linux SSH authentication activity, including:

- Failed SSH authentication attempts
- Successful SSH authentication
- Source IP extraction
- Multiple failures within a short time window
- Successful authentication following repeated failures

An analytics-rule exercise used a threshold of **3 or more failed SSH attempts within 5 minutes**.

## Incident Investigation

Detection rules were used to generate Sentinel incidents. I practised a Tier 1 SOC workflow:

**Triage -> investigate -> assign -> document -> contain/escalate -> close**

I assigned incidents to myself, reviewed the supporting events and practised writing investigation and closure notes.

## Threat Intelligence / Watchlist

I created a **Malicious SSH IPs** watchlist and used it as part of the investigation workflow.

I also practised a containment scenario involving identification of an external suspicious IP and blocking it in the lab environment.

## Microsoft Entra ID Lab

The project was extended into identity monitoring using Microsoft Entra ID.

Exercises included:

- Creating a test tenant
- Creating a test user
- Creating a security group
- Generating successful and failed sign-ins
- Reviewing sign-in logs
- Investigating authentication error **50126**
- Working with Conditional Access

## Skills Demonstrated

- Microsoft Sentinel
- SIEM monitoring
- KQL
- Linux/Syslog monitoring
- Detection engineering fundamentals
- Incident triage and investigation
- SOC documentation
- Watchlists
- Basic containment
- Microsoft Entra ID
- Identity sign-in investigation
- Conditional Access fundamentals

## Repository Structure

- `kql/` - investigation and detection queries
- `detections/` - Sentinel analytics-rule documentation
- `incidents/` - SOC investigation workflow and example documentation
- `watchlists/` - malicious-IP watchlist exercise
- `entra-id/` - identity monitoring and Conditional Access exercises
- `docs/` - architecture and lab notes

## Ethics

All activity documented in this repository was performed in a personal training environment for defensive cybersecurity education.

## Certification

This lab supported my practical preparation for **Microsoft SC-200: Security Operations Analyst**, which I passed in August 2026.
