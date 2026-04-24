# Experiment 06: Email Header & PGP Investigation

## Objective
To analyze email headers to trace the sender's origin and path, and to verify the authenticity and integrity of digitally signed or encrypted messages using PGP (Pretty Good Privacy) tools.

## Tools Used
* **Thunderbird:** For viewing raw email source and header analysis.[Mozilla Thunderbird](https://www.thunderbird.net/en-US/download/)
* **Gpg4win (Kleopatra):** For PGP key management and signature verification.[Gpg4win](https://www.gpg4win.org/download.html)
* **MXToolbox (Header Analyzer):** For visualizing the hop-by-hop relay path.

## Methodology
1. **Header Extraction:** Exported the raw source of a suspicious email (`.eml` format) to inspect the `Received` fields.
2. **Path Tracing:** Identified the originating IP address and the mail servers involved in the relay.
3. **Signature Verification:** Imported a public PGP key into Kleopatra and verified a signed message to ensure it was not modified in transit.
4. **Security Check:** Checked for SPF, DKIM, and DMARC pass/fail statuses in the headers to detect spoofing.

## Results
- **Origin Traced:** The email originated from a server in the Netherlands (`82.94.180.x`).
- **Integrity:** The PGP signature was verified as "Valid," confirming the sender's identity.
