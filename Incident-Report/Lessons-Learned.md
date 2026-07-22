# Lessons Learned

## Overview

This incident highlighted the importance of validating security alerts, investigating persistence mechanisms, and confirming endpoint integrity after malware removal.

---

## Key Findings

- Malwarebytes successfully detected and removed the identified threats.
- Microsoft Defender correctly operated in passive mode because Malwarebytes was registered as the active antivirus solution.
- An orphaned startup registry entry remained after software removal and required manual investigation.
- Scheduled Tasks did not reveal any malicious persistence.
- Npcap was verified as legitimate software rather than an indicator of compromise.
- Windows system corruption identified by SFC was successfully repaired.

---

## Security Improvements

The following actions strengthened the endpoint's security posture:

- Removed unnecessary startup persistence.
- Verified endpoint protection services.
- Confirmed Windows system integrity using DISM and SFC.
- Created a post-remediation Restore Point.
- Performed a final malware validation scan.

---

## Recommendations

To reduce the likelihood of future incidents:

- Keep Windows and applications fully updated.
- Regularly review startup entries and scheduled tasks.
- Perform routine malware scans.
- Enable real-time endpoint protection.
- Maintain current backups and restore points.
- Investigate unexpected persistence mechanisms before removing them.

---

## Analyst Reflection

This investigation reinforced practical skills in:

- Windows Endpoint Investigation
- PowerShell-based Incident Response
- Malware Validation
- Persistence Hunting
- Endpoint Recovery
- Incident Documentation

The investigation followed a structured incident response process from detection through recovery, resulting in a fully restored and validated Windows endpoint.