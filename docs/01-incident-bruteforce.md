## Detection
- SIEM: Wazuh
- Rule Triggered: Logon Failure – Unknown user or bad password
- Rule ID: 60122
- Severity Level: 5
- Associated Windows Event ID: 4625

## Investigation
- Source: Local Windows endpoint
- Agent: windows10-sysmon
- Activity: Multiple failed authentication attempts
- Pattern: Repeated logon failures over a short time window

## Assessment
The activity was confirmed as expected behavior generated during controlled lab testing. No indicators of compromise or unauthorized access were identified.
