# Experiment 03: RAM Capture & Volatile Memory Analysis

## Objective
To capture the volatile memory (RAM) of a live system and analyze it to identify running processes, network connections, and potential malicious activity that would vanish upon a system reboot.

## Tools Used
* **DumpIt:** For memory acquisition (RAM capture). [DumpIt](https://www.comae.com/dumpit/)
* **Volatility 3:** For advanced memory forensics and artifact extraction.[Volatility](https://www.volatilityfoundation.org/releases)

## Methodology
1. **Acquisition:** Executed `DumpIt.exe` on a target Windows 10 machine to generate a `.raw` memory dump.
2. **Profile Identification:** Used Volatility's `windows.info` plugin to determine the OS kernel version.
3. **Process Analysis:** Ran `windows.pslist` and `windows.pstree` to view active and hidden processes.
4. **Network Forensics:** Executed `windows.netscan` to identify established TCP/UDP connections.

## Results
- **Memory Image:** Created `DESKTOP-MEM.raw` (16GB).
- **Findings:** Detected an unauthorized `powershell.exe` process communicating with an external IP address.
