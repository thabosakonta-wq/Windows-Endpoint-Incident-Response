# MITRE ATT&CK Mapping

| Technique | ID | Description |
|-|-|-|
| PowerShell | T1059.001 | Command execution using PowerShell |
| Process Discovery | T1057 | Discovery of running processes |
| File Discovery | T1083 | Searching files and directories |
| Network Service Scanning | T1046 | Network reconnaissance |

---

## Detection Ideas

### PowerShell Monitoring

Monitor:

- Suspicious PowerShell commands
- Encoded commands
- Unusual parent processes

### Process Monitoring

Detect:

- Unknown executables
- Suspicious execution paths
- Abnormal process relationships