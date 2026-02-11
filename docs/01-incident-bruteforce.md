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

## Related Reconnaissance Activity
### Sysmon Process Creation – Account Enumeration

During review of endpoint telemetry, additional process execution activity was observed following authentication failures.

- Event Source: Sysmon
- Event ID: 1 (Process Create)
- Process: net1.exe
- Command Executed: `net user`
- Parent Process: cmd.exe
- User Context: Local interactive user
- Integrity Level: Medium

This activity represents local account enumeration, which is commonly observed during reconnaissance phases of an intrusion. In this lab, the behavior was generated intentionally to validate command-line visibility and process lineage.
