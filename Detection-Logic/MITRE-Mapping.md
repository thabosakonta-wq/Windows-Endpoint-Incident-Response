# MITRE ATT&CK Mapping

## Overview

The investigation identified activities that align with techniques documented in the MITRE ATT&CK framework.

---

| MITRE Technique | Technique ID | Evidence |
|----------------|-------------|----------|
| Registry Run Keys / Startup Folder | T1547.001 | Orphaned Gaijin.Net Updater startup entry |
| Scheduled Task | T1053 | Scheduled Tasks reviewed for persistence |
| System Services | T1543 | Microsoft Defender and Malwarebytes services validated |
| Windows Command Shell | T1059.003 | PowerShell used throughout the investigation |
| File and Directory Discovery | T1083 | Validation of executable paths using Test-Path |
| Indicator Removal on Host | T1070 | Registry persistence removed |
| System Recovery | T1490 | Restore Point created after remediation |

---

## Detection Opportunities

SOC analysts should monitor:

- New Registry Run keys
- Scheduled Task creation
- Unexpected service installation
- PowerShell execution
- Unexpected startup entries
- Antivirus status changes

---

## Defensive Recommendations

- Monitor PowerShell logging.
- Enable Microsoft Defender Tamper Protection.
- Review startup registry locations regularly.
- Investigate orphaned startup entries.
- Review scheduled tasks periodically.
- Maintain endpoint protection and patching.

---

## ATT&CK Coverage

The investigation primarily covered:

- Persistence
- Defense Evasion
- Discovery
- Execution