# PowerShell Suspicious Execution Case Study

## Incident Summary

A suspicious PowerShell execution alert was triggered on a Windows endpoint.

## Alert Source

Microsoft Sentinel / Endpoint Detection

## Investigation

Reviewed:

- Windows Event ID 4688
- PowerShell Operational Logs
- Sysmon Event ID 1
- Network connections

## Findings

Observed suspicious PowerShell activity requiring investigation.

## MITRE ATT&CK Mapping

Technique:

T1059.001 PowerShell

## Response Actions

- Investigated process execution
- Collected evidence
- Analysed indicators
- Created detection logic

## Lessons Learned

Improved visibility into PowerShell abuse and endpoint monitoring.