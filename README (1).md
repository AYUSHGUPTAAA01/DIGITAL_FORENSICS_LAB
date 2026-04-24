# Digital Forensics Lab — 8 Experiments

A complete collection of digital forensics experiments covering disk imaging, file recovery, memory analysis, timeline generation, metadata extraction, email forensics, browser forensics, and Android forensics.

---

## Repository Structure

```
digital_forensics/
├── exp1_disk_imaging/
│   ├── disk_imaging.sh
│   └── README.md
├── exp2_file_recovery/
│   ├── recover_files.py
│   └── README.md
├── exp3_memory_analysis/
│   ├── memory_analysis.py
│   └── README.md
├── exp4_timeline/
│   ├── generate_timeline.py
│   └── README.md
├── exp5_metadata/
│   ├── extract_metadata.py
│   └── README.md
├── exp6_email_forensics/
│   ├── email_forensics.py
│   └── README.md
├── exp7_browser_forensics/
│   ├── browser_forensics.py
│   └── README.md
├── exp8_android_forensics/
│   ├── android_forensics.py
│   └── README.md
└── README.md  ← You are here
```

---

## Experiment List

| # | Experiment | Tool / Script | Key Concepts |
|---|-----------|---------------|-------------|
| 1 | Disk Imaging | `disk_imaging.sh` | dd, dcfldd, MD5/SHA256 verification |
| 2 | Deleted File Recovery | `recover_files.py` | File carving, Foremost, Scalpel, magic bytes |
| 3 | RAM Capture & Memory Analysis | `memory_analysis.py` | Volatility 3, pslist, netstat, strings |
| 4 | Forensic Timeline Generation | `generate_timeline.py` | MAC times, mactime, Plaso/log2timeline |
| 5 | Metadata Extraction | `extract_metadata.py` | EXIF, PDF metadata, Office metadata, ExifTool |
| 6 | Email Forensics | `email_forensics.py` | Header analysis, spoofing detection, attachments |
| 7 | Browser Forensics | `browser_forensics.py` | Chrome/Firefox SQLite, history, cookies, downloads |
| 8 | Android Forensics | `android_forensics.py` | ADB, SMS, call logs, SQLite databases |

---

## Requirements

### System
- Linux (Ubuntu 20.04+ or Kali Linux recommended)
- Python 3.8 or higher
- `sudo` / root privileges for some experiments

### Python Libraries
Install all optional dependencies at once:
```bash
pip install piexif Pillow pypdf
```

### System Tools (install as needed)
```bash
sudo apt update
sudo apt install -y adb foremost scalpel dcfldd exiftool sqlite3
```

### Volatility 3 (for Experiment 3)
```bash
git clone https://github.com/volatilityfoundation/volatility3
cd volatility3
pip install -r requirements.txt
```

---

## Quick Start

### Run all experiments in sequence:
```bash
# Experiment 1 — Disk Imaging
cd exp1_disk_imaging
sudo bash disk_imaging.sh

# Experiment 2 — File Recovery
cd ../exp2_file_recovery
python3 recover_files.py

# Experiment 3 — Memory Analysis
cd ../exp3_memory_analysis
python3 memory_analysis.py

# Experiment 4 — Timeline Generation
cd ../exp4_timeline
python3 generate_timeline.py

# Experiment 5 — Metadata Extraction
cd ../exp5_metadata
python3 extract_metadata.py

# Experiment 6 — Email Forensics
cd ../exp6_email_forensics
python3 email_forensics.py

# Experiment 7 — Browser Forensics
cd ../exp7_browser_forensics
python3 browser_forensics.py

# Experiment 8 — Android Forensics
cd ../exp8_android_forensics
python3 android_forensics.py
```

> All scripts run in **demo mode** by default — no real device or disk image required.

---

## Experiment Summaries

### Experiment 1 — Disk Imaging
Creates a forensic bit-by-bit copy of a storage device using `dd`. Verifies integrity by comparing MD5 and SHA256 hashes of the source and the image.

**Output:** `disk_image.dd`, `image_hash.txt`, `imaging_log.txt`

---

### Experiment 2 — Deleted File Recovery
Recovers deleted files from a disk image by scanning for file magic bytes (headers/footers). Supports JPEG, PNG, PDF, ZIP, and more. Also integrates with `foremost` and `scalpel`.

**Output:** `recovered_files/`, `recovery_log.txt`

---

### Experiment 3 — RAM Capture & Memory Analysis
Captures a live memory dump (using LiME on Linux or DumpIt on Windows) and analyzes it using Volatility 3. Extracts running processes, network connections, password hashes, and injected code.

**Output:** `memory_output/pslist.json`, `netstat.txt`, `strings.txt`

---

### Experiment 4 — Forensic Timeline Generation
Collects MAC (Modified, Accessed, Changed) timestamps from all files in a directory and generates a sorted forensic timeline. Flags anomalies such as future timestamps and suspicious executables.

**Output:** `timeline_output/timeline.csv`, `timeline.json`, `timeline_report.txt`

---

### Experiment 5 — Metadata Extraction
Extracts hidden metadata from JPEG images (EXIF — camera, GPS, timestamps), PDF documents (author, creator, software), and Office files (docx/xlsx — last editor, revision count, company).

**Output:** `metadata_output/metadata_report.json`

---

### Experiment 6 — Email Forensics
Analyzes raw email (.eml) files to trace the routing path through `Received` headers, detect spoofing by comparing From/Reply-To/Return-Path domains, extract attachments with hash values, and identify suspicious URLs.

**Output:** `email_output/email_report.json`, extracted attachments

---

### Experiment 7 — Browser Forensics
Extracts forensic artifacts from Chrome and Firefox SQLite databases including full browsing history with timestamps, file downloads with source URLs, and session cookies. Flags suspicious executable downloads.

**Output:** `browser_output/browser_report.json`

---

### Experiment 8 — Android Forensics
Uses ADB (Android Debug Bridge) to connect to an Android device, extract device information, pull SMS/MMS databases, call logs, and application data. Parses SQLite databases to reconstruct communication history.

**Output:** `android_output/android_report.json`, `databases/`

---

## Tools Reference

| Tool | Purpose | Install |
|------|---------|---------|
| `dd` | Disk imaging | Pre-installed on Linux |
| `dcfldd` | Forensic dd with hashing | `sudo apt install dcfldd` |
| `foremost` | File carving | `sudo apt install foremost` |
| `scalpel` | File carving | `sudo apt install scalpel` |
| `volatility3` | Memory analysis | `pip install volatility3` |
| `exiftool` | Metadata extraction | `sudo apt install libimage-exiftool-perl` |
| `adb` | Android forensics | `sudo apt install adb` |
| `sqlite3` | Database analysis | `sudo apt install sqlite3` |
| `mactime` | Timeline generation | Part of The Sleuth Kit |

---

## Notes

- All scripts include a **demo mode** that creates sample data automatically so they can be run and demonstrated without real devices or evidence files.
- Never perform forensic analysis on original evidence — always work on a verified copy.
- Hash verification (MD5 + SHA256) should be performed before and after every acquisition.
- Scripts are for **educational purposes** in a controlled lab environment.

---

## References

- NIST SP 800-86: Guide to Integrating Forensic Techniques into Incident Response
- Carrier, B. (2005). *File System Forensic Analysis*
- Ligh, M. H. et al. (2014). *The Art of Memory Forensics*
- Casey, E. (2011). *Digital Evidence and Computer Crime*
- Volatility Foundation: https://github.com/volatilityfoundation/volatility3
- The Sleuth Kit: https://www.sleuthkit.org
- ExifTool: https://exiftool.org

---

*Digital Forensics Lab | Academic Use Only*
