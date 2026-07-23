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

### Malwarebytes Detection

Threat Scan Summary

![Threat Scan](Screenshots/Malwarebytes/01-Threat-Scan.jpg)

Detected Threats

![Detected Threats](Screenshots/Malwarebytes/02-Detected-Threats.jpg)

Threats Quarantined

![Quarantine](Screenshots/Malwarebytes/03-Quarantine.jpg)

---

### Microsoft Defender Validation

Windows Security Dashboard

![Windows Security](Screenshots/Defender/01-Windows-Security.jpg)

Defender Status (PowerShell)

![Defender Status](Screenshots/Defender/02-Defender-Status-PowerShell.jpg)

Defender Service

![WinDefend Service](Screenshots/Defender/03-WinDefend-Service.jpg)

---

### PowerShell Investigation

Startup Registry Review

![Startup Registry](Screenshots/PowerShell/01-Startup-Registry.jpg)

Scheduled Tasks Review

![Scheduled Tasks](Screenshots/PowerShell/02-Scheduled-Tasks.jpg)

Registered Antivirus Products

![Antivirus Products](Screenshots/PowerShell/04-Antivirus-Products.jpg)

Service Events

![Service Events](Screenshots/PowerShell/05-Service-Events.jpg)

---

### Windows System Repair

DISM Repair

![DISM](Screenshots/SFC-DISM/01-DISM-RestoreHealth.jpg)

SFC Validation

![SFC](Screenshots/SFC-DISM/02-SFC-Scan.jpg)

---

### Recovery

Restore Point Created

![Restore Point](Screenshots/Restore-Point/01-Restore-Point-List.jpg)

System Protection

![System Protection](Screenshots/Restore-Point/02-System-Protection.jpg)

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
