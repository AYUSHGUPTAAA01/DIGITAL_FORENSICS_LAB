Digital Forensics Laboratory

A comprehensive portfolio of forensic investigations, evidence acquisition, artifact analysis, and incident reconstruction.

Project Overview:
This repository serves as a technical log for the Digital Forensics (DFT) Lab. It documents the acquisition, preservation, analysis, and reporting of digital evidence using industry-standard forensic tools and methodologies.

Experiment Index
1: Forensic Disk Imaging & Integrity Verification

Objective: Create a forensic disk image using FTK Imager or Guymager and verify its integrity using SHA-256 hashing.
Focus: Learning to acquire a forensically sound image of a storage device while maintaining evidence integrity through cryptographic hash verification.

2: Deleted File Recovery & Metadata Analysis

Objective: Recover deleted files and inspect metadata from a disk image using Autopsy and Sleuth Kit.
Focus: Exploring deleted content recovery and analyzing timestamps, ownership, and file access patterns for digital evidence.

3: Memory Forensics (RAM Analysis)

Objective: Capture and analyze RAM using DumpIt and Volatility to extract process and network data.
Focus: Investigating volatile memory to identify running processes, open network connections, hidden malware, and suspicious activities.

4: Timeline Analysis from File System Metadata

Objective: Generate a system timeline using Plaso or Autopsy.
Focus: Creating a chronological view of system events based on creation, modification, and access timestamps to detect anomalous behavior.

5: Metadata Extraction from Media & Documents

Objective: Extract and analyze metadata from images and documents using ExifTool and PDFinfo.
Focus: Discovering hidden information such as author details, timestamps, GPS locations, and document history for forensic investigations.

6: Email Header & PGP Investigation

Objective: Investigate email headers and PGP-signed messages using Thunderbird and Gpg4win.
Focus: Tracing sender routes, identifying originating IP addresses, and verifying message authenticity using digital signatures and encryption tools.

7: Browser Artifact Inspection

Objective: Examine browser history, cache, and cookies using Browser History Examiner or Nirsoft tools.
Focus: Recovering browsing artifacts such as visited URLs, cached content, and cookies to understand user behavior and possible compromise points.

8: Android Device Forensics

Objective: Analyze an Android device image using Andriller or Autopsy.
Focus: Extracting call logs, SMS messages, app data, saved credentials, and other mobile artifacts for forensic analysis.

9: Hash-Based File Integrity Verification

Objective: Perform hash-based file comparison using sha256sum and md5deep.
Focus: Generating and comparing cryptographic hashes to detect tampering, unauthorized modifications, and integrity violations.

10: Incident Reconstruction & Log Correlation

Objective: Correlate system and network logs using Timesketch.
Focus: Aggregating multiple evidence sources to reconstruct security incidents, establish event timelines, and prepare professional forensic reports.

Tech Stack & Tools:
>> Disk & File Forensics
>> FTK Imager, Guymager, Autopsy, Sleuth Kit, sha256sum, md5deep
>> Memory Forensics
>> DumpIt, Volatility
>> Metadata Analysis
>> ExifTool, PDFinfo
>> Email & Communication Analysis
>> Thunderbird, Gpg4win
>> Browser & Mobile Forensics
>> Browser History Examiner, Nirsoft Tools, Andriller
>> Timeline & Incident Analysis
>> Plaso, Timesketch

Methodologies

Evidence Preservation, Hash Verification, Timeline Analysis, Chain of Custody, Incident Reconstruction

