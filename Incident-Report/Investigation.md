# Investigation

## Objective

Investigate suspicious malware detections, identify persistence mechanisms, validate endpoint integrity, and confirm successful remediation.

---

## Initial Findings

Malwarebytes detected multiple malicious and potentially unwanted objects during the initial endpoint scan.

Primary detections included:

- Trojan.FakeChrome
- PUP.Optional.DriverPack

The endpoint required validation to determine whether any persistence mechanisms remained active.

---

## Microsoft Defender Validation

The Microsoft Defender service was confirmed to be running.

PowerShell command:

Get-Service WinDefend

Further validation showed Microsoft Defender operating in passive mode because Malwarebytes was registered as the active antivirus solution.

PowerShell command:

Get-MpComputerStatus

Observed state:

- Antivirus Enabled
- Real-Time Protection Disabled
- Passive Mode (SxS)

This behavior is expected when Malwarebytes is the primary AV.

---

## Malwarebytes Validation

Confirmed Malwarebytes Service was running.

PowerShell command:

Get-Service MBAMService

Malwarebytes remained responsible for real-time malware protection.

---

## Startup Persistence Investigation

Registry startup entries were reviewed.

PowerShell command:

Get-ItemProperty HKCU:\Software\Microsoft\Windows\CurrentVersion\Run

Findings:

One startup entry referenced:

Gaijin.Net Updater

The executable no longer existed.

Validation command:

Test-Path

Result:

False

This confirmed the registry entry was orphaned persistence.

The registry entry was safely removed.

---

## Scheduled Task Review

Scheduled Tasks were inspected for suspicious update mechanisms.

PowerShell command:

Get-ScheduledTask

No malicious scheduled tasks were identified.

All tasks were consistent with Windows, Microsoft Edge, Opera, and OneDrive.

---

## Npcap Verification

Npcap service was verified.

PowerShell command:

Get-Service npcap

Npcap installation path was reviewed.

No indicators suggested compromise.

Npcap was determined to be legitimate software required by packet capture tools.

---

## Windows Integrity Verification

DISM completed successfully.

SFC identified corrupted Windows system files and repaired them successfully.

System integrity was restored.

---

## Restore Point Verification

A restore point was created after remediation.

PowerShell command:

Get-ComputerRestorePoint

The restore point was successfully created.

---

## Final Validation

Malwarebytes Deep Scan

Objects Scanned:

420,055

Threats Remaining:

0

The endpoint showed no remaining persistence, malware, or integrity issues.