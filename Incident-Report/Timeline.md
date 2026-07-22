# Incident Timeline

| Time | Activity |
|------|----------|
| Initial Investigation | Malwarebytes detected Trojan.FakeChrome and PUP.Optional.DriverPack |
| Investigation Started | Microsoft Defender service status verified |
| Defender Validation | Microsoft Defender found to be operating in passive mode alongside Malwarebytes |
| Persistence Hunt | Startup registry entries reviewed |
| Registry Finding | Orphaned Gaijin.Net Updater startup entry discovered |
| Remediation | Invalid registry persistence removed |
| Scheduled Tasks Review | No suspicious scheduled tasks identified |
| Npcap Validation | Npcap installation verified as legitimate |
| System Integrity | DISM executed successfully |
| System Integrity | SFC repaired Windows Resource Protection violations |
| Endpoint Validation | Malwarebytes Deep Scan completed with zero remaining threats |
| Recovery | Restore Point created after remediation |
| Incident Closed | Endpoint returned to trusted operational state |