## Investigative Timeline Analysis

| Window of Interest | Observation |
| :--- | :--- |
| **10:45 - 10:46** | User 'Admin' accessed and then deleted sensitive documentation. |
| **10:48** | System logs were intentionally stopped (Anti-forensics technique). |
| **10:50** | A persistence mechanism (Registry Run Key) was established for an unknown executable. |

### Conclusion
The timeline reveals a classic "Data Theft" pattern. The user accessed the file, deleted it to hide tracks, and then disabled logging before installing a persistence mechanism. The use of **Plaso** allowed us to see these different types of artifacts (LNK files, MFT, and Registry) in one single, unified stream of time.
