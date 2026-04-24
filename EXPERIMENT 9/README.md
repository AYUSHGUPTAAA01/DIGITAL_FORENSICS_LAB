# Experiment 09: Hash-Based File Comparison & Integrity Verification

## Objective
To generate and compare cryptographic hashes of individual files to verify their integrity and identify tampered or unauthorized changes. This experiment focuses on using hashing as a method for rapid file identification and verification of evidence.

## Tools Used
* **sha256sum:** Standard Linux/Unix tool for SHA-256 hash generation.
* **md5deep / hashdeep:** For recursive hashing of entire directories.[hashdeep / md5deep](https://github.com/jessek/hashdeep)

## Methodology
1. **Baseline Generation:** Created a hash manifest of a "clean" set of system files.
2. **Comparison:** Modified a single byte within a configuration file and re-hashed it to observe the "Avalanche Effect."
3. **Verification:** Used `sha256sum -c` to automatically check a list of files against a known-good manifest.
4. **Collision Testing:** Discussed why MD5 is no longer sufficient for high-security environments compared to SHA-256.

## Results
- **Detection:** Successfully identified three files that were modified by the "wiping" utility found in Experiment 07.
- **Accuracy:** Proven that hashing can detect even a 1-bit change in a 1GB file.
