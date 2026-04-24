# Experiment 02: File Recovery & Metadata Analysis

## Objective
To explore the recovery of deleted content from a forensic disk image and analyze file system metadata (MAC times, permissions, and ownership) to reconstruct user activity.

## Tools Used
* **Autopsy Forensic Browser** [Autopsy](https://www.autopsy.com/download/)
* **The Sleuth Kit (TSK)** [The Sleuth Kit](https://www.sleuthkit.org/)

## Methodology
1. **Case Creation:** Imported the E01 image created in Experiment 01 into Autopsy.
2. **Ingest Modules:** Ran "File Recovery" and "Recent Activity" modules to parse the file system.
3. **Data Carving:** Used signatures to identify and recover files that were unlinked from the File Allocation Table (FAT) or Master File Table (MFT).
4. **Metadata Inspection:** Analyzed the `$Data` and `$Standard_Information` attributes of recovered files.

## Results
- **Recovery:** Successfully recovered 14 deleted JPG images and 2 PDF documents.
- **Artifacts:** Identified the original file creation and deletion timestamps.
