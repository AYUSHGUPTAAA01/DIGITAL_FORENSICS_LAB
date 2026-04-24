## Web Artifact Analysis Report

| Artifact Category | Findings |
| :--- | :--- |
| **Primary Browser** | Google Chrome (v124.x) |
| **Suspicious Activity** | Download of "Eraser" utility (Anti-forensics tool). |
| **Data Leakage Site** | `mega.nz` accessed at 11:20 AM. |
| **Session Persistence** | Active cookies found for ProtonMail. |

### Investigative Summary
The browser history indicates a high level of technical intent. The user searched for methods to securely delete files and then downloaded a known "wiping" utility. Furthermore, the access to a cloud storage provider (`mega.nz`) coincides with the file deletions identified in **Experiment 02**.

**Conclusion:** The web artifacts provide a motive and a method for the data destruction observed during the investigation. The "Typed Count" of 1 for the cloud storage URL suggests the user entered the address directly, rather than following a link.
