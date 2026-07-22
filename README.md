# Windows Endpoint Incident Response

## Overview

This repository documents a complete Windows Endpoint Incident Response investigation involving malware detection, persistence hunting, system remediation, and post-incident validation.

## Incident

Trojan.FakeChrome
PUP.Optional.DriverPack

## Skills Demonstrated

- Malware Investigation
- Endpoint Detection
- Persistence Hunting
- Windows Registry Analysis
- Scheduled Task Analysis
- Microsoft Defender Validation
- Malwarebytes Investigation
- Windows System Repair
- MITRE ATT&CK Mapping
- Incident Documentation

## Repository Structure

Incident-Report/
Detection-Logic/
Evidence/
Screenshots/

## Tools Used

- Malwarebytes
- Microsoft Defender
- PowerShell
- DISM
- SFC
- Registry Editor
- Task Scheduler

## MITRE ATT&CK

Tactic and technique mapping available under Detection-Logic.

| Technique | ID |
|---|---|
| PowerShell | T1059.001 |
| Process Discovery | T1057 |
| File and Directory Discovery | T1083 |
| Network Service Scanning | T1046 |

---

## Skills Demonstrated

- Windows Endpoint Investigation
- Digital Forensics Fundamentals
- Threat Detection
- Incident Response Documentation
- MITRE ATT&CK Mapping
- SOC Analyst Workflow

----

## Investigation Screenshots

### Windows Event Investigation

![Windows Event Investigation](Screenshots/event-viewer.png)

### Sysmon Process Analysis

![Sysmon Analysis](Screenshots/sysmon-event.png)

----

## Microsoft Sentinel Detection Engineering

The investigation was extended into Microsoft Sentinel using KQL detection logic.

Implemented detections:

- Suspicious PowerShell execution
- Failed login detection
- Process creation monitoring
- Threat hunting queries

Example KQL Detection:

```kql
SecurityEvent
| where EventID == 4688
| where CommandLine contains "powershell"
| project TimeGenerated, Computer, Account, CommandLine

----

### Detection Mapping

| Detection | MITRE ATT&CK |
|---|---|
| Suspicious PowerShell | T1059.001 |
| Process Creation | T1057 |
| Failed Authentication | T1110 |

----

## Sysmon Endpoint Monitoring

Sysmon was deployed on the Windows endpoint to collect detailed security telemetry.

Collected evidence includes:

- Process creation monitoring (Event ID 1)
- Parent-child process relationships
- Command-line analysis
- SHA256 file hashes
- User and integrity level analysis

Example investigation:

A Firefox process creation event was captured using Sysmon Event ID 1 and analysed through Windows Event Viewer.

Evidence location:

----

MITRE ATT&CK mapping:

- T1059 - Command and Scripting Interpreter
- T1106 - Native API

----

## Evidence Screenshots

### Sysmon Event ID 1 - Process Creation

![Sysmon Event ID 1](Evidence/Sysmon/Screenshots/sysmon-event-id-1.png)

### Sysmon Process Creation Investigation

![Sysmon Process Creation](Evidence/Sysmon/Screenshots/sysmon-process-create.png)

----

# Author

**Thabo Sakonta**

Microsoft Certified Security Operations Analyst (SC-200)

LinkedIn

https://www.linkedin.com/in/thabo-sakonta-377a3748

GitHub

https://github.com/thabosakonta-wq

---

# License

Educational and portfolio purposes.
