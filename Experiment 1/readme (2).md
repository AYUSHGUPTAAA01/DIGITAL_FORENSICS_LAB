# Experiment 1: Forensic Disk Imaging & Integrity Verification

## Objective
To acquire a bit-for-bit physical image of a storage device and verify its integrity using SHA-256 hashing to ensure the evidence remains unaltered.

## Tools Used
* **FTK Imager v4.5** [FTK Imager v4.5](https://www.exterro.com/ftk-product-downloads/ftk-imager-version-4-7-3)
* **HashCalc** (for secondary verification) [HashCalc](https://guymager.sourceforge.io/)

## Process Summary
1.  Connected a 4GB USB Flash Drive as the evidence source.
2.  Used FTK Imager to create a **Physical Image** in **E01 (EnCase)** format.
3.  Set compression level to 6 and enabled hash verification.
4.  Generated a SHA-256 hash during the acquisition phase to establish a "digital fingerprint."

## Findings
The image was successfully created and verified. The computed hash matches the source drive, confirming a successful bit-stream acquisition.
