# Experiment 04: System Timeline Generation & Analysis

## Objective
To reconstruct a chronological narrative of system events by aggregating metadata from various sources (MFT, Registry, Event Logs). This helps identify the exact moment of compromise or unauthorized user activity.

## Tools Used
* **Plaso (log2timeline):** To extract and aggregate timestamps. [Plaso](https://plaso.readthedocs.io/en/latest/sources/user/Installing.html)
* **Autopsy Timeline Tool:** For visual analysis of event clusters.[Autopsy](https://www.autopsy.com/download/)

## Methodology
1. **Extraction:** Ran `log2timeline.py` against the disk image created in Experiment 01.
2. **Storage:** Generated a `.plaso` storage file containing all extracted events.
3. **Filtering:** Used `psort.py` to filter the timeline for a specific window of interest (e.g., the 2 hours surrounding the suspected incident).
4. **Analysis:** Visualized the data in Autopsy to look for "Event Pulses"—large spikes in file modifications or deletions.

## Results
- **Timeline Export:** Generated a 15,000-line CSV of system events.
- **Key Discovery:** Identified a series of "File Create" events in the System32 folder followed immediately by "Registry Key Modified" events.
