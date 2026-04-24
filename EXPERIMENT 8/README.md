# Experiment 08: Android Device Forensics

## Objective
To analyze an Android logical/physical image to retrieve user data such as call logs, SMS messages, and application-specific data (WhatsApp/Telegram). This helps in reconstructing mobile-based communications and location history.

## Tools Used
* **Andriller:** For parsing Android backup files and communications.[Andriller](https://sourceforge.net/projects/andriller/)
* **Autopsy (Android Analyzer):** For automated parsing of the filesystem.[Autopsy](https://www.autopsy.com/download/)
* **DB Browser for SQLite:** To manually inspect message databases.

## Methodology
1. **Image Acquisition:** Used a forensic image of an Android device (Physical dump).
2. **Database Extraction:** Located key databases like `mmssms.db` (SMS) and `contacts2.db` (Contacts).
3. **App Analysis:** Parsed the `/data/data/` directory to find third-party application artifacts.
4. **Credential Extraction:** Inspected the `accounts.db` file to identify linked Google and Social Media accounts.

## Results
- **SMS Recovery:** Extracted 150+ messages, including several deleted threads.
- **Call History:** Identified frequent contact with a suspicious international number.
