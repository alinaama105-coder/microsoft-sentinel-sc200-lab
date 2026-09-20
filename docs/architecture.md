# SC-200 Lab Architecture

```text
                   Microsoft Azure
                         |
                    +----------+
                    | Linux VM |
                    +----------+
                         |
                       Syslog
                         |
                         v
                +-----------------+
                | Log Analytics   |
                | Workspace       |
                +-----------------+
                         |
                         v
                +-----------------+
                | Microsoft       |
                | Sentinel        |
                +-----------------+
                  /      |       \
                 /       |        \
               KQL   Analytics   Watchlist
                      Rules
                         |
                         v
                     Incidents
                         |
                         v
             Triage / Investigation
                         |
                         v
              Containment / Closure


        Microsoft Entra ID Practice Environment
                         |
              +----------+----------+
              |                     |
         Sign-in Logs        Conditional Access
              |
              v
       Identity Investigation
```

## Project Progression

The lab was deliberately built in stages:

1. Deploy and access an Azure Linux VM.
2. Connect Linux/Syslog telemetry.
3. Investigate authentication activity using KQL.
4. Build detection logic.
5. Generate and handle Sentinel incidents.
6. Add watchlist context and containment exercises.
7. Extend monitoring into Microsoft Entra ID identity events.

This provided an end-to-end introduction to the workflow expected in a security operations environment.
