## Metadata Findings Report

| Artifact Type | Evidence Finding |
| :--- | :--- |
| **File System** | NTFS |
| **Recovery Method** | PhotoRec / Autopsy Carver |
| **Evidence Found** | Deleted PDF containing corporate strategy. |
| **Timestamps** | Modification occurred 2 hours prior to deletion. |

### Metadata Insight:
Using the **Sleuth Kit (istat)**, we analyzed the MFT entry for the recovered PDF. 
- **MFT Entry:** 542
- **Sequence Number:** 2
- **Flags:** Not in Use (Deleted)

**Conclusion:** The presence of specific file fragments in unallocated space indicates an intentional attempt to wipe data before the device was seized. Metadata confirms the files were accessed by the user `Admin-PC` shortly before the deletion event.
