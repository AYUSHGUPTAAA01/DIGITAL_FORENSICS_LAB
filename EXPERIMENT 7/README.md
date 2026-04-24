# Experiment 07: Browser History & Artifact Analysis

## Objective
To recover and analyze web browsing artifacts, including visited URLs, search queries, cached images, and cookies. This data is essential for understanding user behavior and identifying potential sources of malware or unauthorized data exfiltration.

## Tools Used
* **NirSoft BrowsingHistoryView:** To aggregate history from multiple browsers.[Browser History Examiner](https://www.foxtonforensics.com/browser-history-examiner/)
* **ChromeCacheView:** To inspect files stored in the browser's local cache.
* **DB Browser for SQLite:** To manually query the underlying browser databases.
[NirSoft Browser Tools](https://www.nirsoft.net/web_browser_tools.html)
## Methodology
1. **Locating Databases:** Navigated to the user profile path: `\AppData\Local\Google\Chrome\User Data\Default\`.
2. **History Extraction:** Loaded the `History` SQLite database into BrowsingHistoryView to see the chronological list of visits.
3. **Cache Analysis:** Used ChromeCacheView to find thumbnails of images viewed by the user, even if the original website is now offline.
4. **Cookie Inspection:** Analyzed the `Cookies` database to identify session information and potential account access.

## Results
- **Evidence Found:** Identified a visit to a "Temporary File Upload" site just minutes before the disk was imaged.
- **Search Queries:** Recovered Google searches for "how to wipe a hard drive" and "anonymous VPNs."
