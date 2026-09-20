# Malicious SSH IP Watchlist Exercise

## Objective

Practise using Microsoft Sentinel watchlists to provide additional context during investigations.

## Watchlist

A watchlist named:

**Malicious SSH IPs**

was created for the lab.

## Workflow

```text
SSH event
   |
   v
Extract / identify source IP
   |
   v
Compare with watchlist
   |
   v
Add context to investigation
   |
   v
Decide on escalation / containment
```

## Learning Outcome

The exercise demonstrated how external or internally maintained indicator lists can enrich a SIEM investigation and help an analyst correlate an observed entity with known context.

The IP data used in this exercise belonged to the training scenario and is not published here as a claim about any real-world address.
