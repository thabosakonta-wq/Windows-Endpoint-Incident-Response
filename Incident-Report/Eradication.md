# Eradication

## Objective

Completely remove malicious software, eliminate persistence mechanisms, and restore system integrity.

---

## Malware Removal

Malwarebytes was used to quarantine and remove all detected threats.

Primary detections included:

- Trojan.FakeChrome
- PUP.Optional.DriverPack

All detected malicious objects were successfully removed.

---

## Registry Cleanup

The following orphaned persistence entry was removed:

Registry Path:

HKCU\Software\Microsoft\Windows\CurrentVersion\Run

Registry Entry:

Gaijin.Net Updater

The executable referenced by this entry no longer existed.

The registry value was removed using PowerShell.

---

## Windows Repair

Windows integrity was restored using built-in repair tools.

### Deployment Image Servicing and Management (DISM)

Command executed:

```powershell
DISM /Online /Cleanup-Image /RestoreHealth
```

Result:

Completed successfully.

---

### System File Checker (SFC)

Command executed:

```powershell
sfc /scannow
```

Result:

Windows Resource Protection found corrupt files and successfully repaired them.

---

## Endpoint Validation

Additional verification included:

- Microsoft Defender status
- Malwarebytes service status
- Registry review
- Scheduled Tasks review
- Npcap validation

No further indicators of compromise were identified.

---

## Eradication Result

Malware was successfully removed.

Persistence mechanisms were eliminated.

System integrity was restored.

The endpoint was ready for recovery.