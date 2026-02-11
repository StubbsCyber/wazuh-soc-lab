# Environment Baseline

## Purpose
This document establishes the current-state baseline of the SOC lab environment.
The focus is on visibility, log ingestion, and agent connectivity rather than initial build steps.

## Wazuh SIEM
- Deployment Type: All-in-One
- Operating System:
- Wazuh Version:
- Hostname:
- IP Address:

### Services Status
- wazuh-manager: Running
- wazuh-indexer: Running
- wazuh-dashboard: Running

## Endpoints
### Windows Endpoint 1
- Hostname: windows10-sysmon
- OS Version: Windows 10 Pro 10.0.19045.6456
- Wazuh Agent Status: Active
- Sysmon Installed: Yes 

### Windows Endpoint 2
- Hostname:
- OS Version:
- Wazuh Agent Status:
- Sysmon Installed: Yes / No

## Initial Observations
- Agents connectivity status
- Logs currently visible
- Any gaps identified

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
