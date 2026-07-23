# Executive Summary

## Incident

On 18 July 2026, Malwarebytes detected multiple malicious and potentially unwanted objects on a Windows 10 endpoint.

### Primary Detections

- Trojan.FakeChrome
- PUP.Optional.DriverPack

A total of **43 malicious objects** were detected during the initial scan.

### Malware Detection Summary

A manual Malwarebytes Threat Scan identified **43 malicious and potentially unwanted artifacts** affecting the endpoint.

The detections included:

- Trojan.FakeChrome
- Trojan.SearcherBar
- PUP.Optional.DriverPack
- PUP.Optional.InternetStart

The identified threats affected:

- Registry Run Keys
- Startup persistence
- Browser configuration
- Local application folders
- Microsoft Edge user profile data

All detected threats were successfully quarantined and validated during the eradication phase.

---

## Investigation

The endpoint investigation included:

- Validation of Microsoft Defender status
- Validation of Malwarebytes protection
- Windows Registry startup review
- Scheduled Task review
- Persistence hunting
- Npcap verification
- Windows integrity verification using DISM and SFC

An orphaned registry startup entry for **Gaijin.Net Updater** was identified and removed after confirming the executable no longer existed.

---

## Remediation

The following remediation actions were completed:

- Malware quarantined and removed
- Windows system repaired using DISM
- Windows Resource Protection repaired corrupted files using SFC
- Registry persistence removed
- Restore point created after remediation
- Deep malware scan performed

---

## Validation

The final Malwarebytes Deep Scan reported:

- Objects Scanned: 420,055
- Threats Detected: 0
- Threats Quarantined: 0

The endpoint was returned to a trusted operational state.

### Microsoft Defender Validation

Windows Security recognised both Malwarebytes and Microsoft Defender.

During post-remediation validation, the Microsoft Defender Antivirus service remained stopped while Malwarebytes was registered as the active endpoint protection solution.

No evidence was found that Microsoft Defender had been disabled through Group Policy. Windows Security remained operational throughout the investigation.

---

## Incident Status

**Status:** Closed

The investigation confirmed successful malware removal, persistence cleanup, endpoint validation, and recovery.