## Volatile Evidence Report

| Artifact | Data Found |
| :--- | :--- |
| **Capture Tool** | DumpIt.exe |
| **Analysis Framework** | Volatility 3 |
| **Suspicious PID** | 4812 (powershell.exe) |
| **Remote C2 IP** | 104.21.45.12 |

### Investigative Summary
Analysis of the RAM dump revealed a PowerShell instance (PID 4812) that was launched by a user session. The network scan confirmed this process had an active encrypted connection to an external IP address (104.21.45.12). 

**Conclusion:** This behavior is consistent with a **Reverse Shell** or data exfiltration. Because this data exists only in RAM, it would have been lost if the machine was powered off before imaging.
