# Containment

## Objective

Prevent additional malicious activity while preserving evidence for investigation.

---

## Immediate Actions

The following containment actions were performed:

- Malwarebytes quarantine executed
- Microsoft Defender status verified
- Endpoint remained isolated from additional malware execution
- Registry startup entries reviewed
- Suspicious persistence investigated

---

## Registry Persistence Removal

An orphaned startup registry entry was discovered.

Registry Location:

HKCU\Software\Microsoft\Windows\CurrentVersion\Run

Entry:

Gaijin.Net Updater

Validation confirmed the executable no longer existed.

PowerShell command used:

Test-Path

Result:

False

The startup entry was removed.

---

## Scheduled Tasks

Scheduled Tasks were inspected for persistence.

No malicious scheduled tasks were identified.

---

## Service Validation

Verified the following services:

- Malwarebytes Service
- Microsoft Defender Service
- Npcap Service

No unauthorized services were identified.

---

## Containment Result

No active persistence remained following registry cleanup.

The endpoint was ready for eradication activities.