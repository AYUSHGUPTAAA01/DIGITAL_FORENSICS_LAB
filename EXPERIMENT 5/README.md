# Experiment 05: Media & Document Metadata Extraction

## Objective
To extract and analyze hidden metadata from digital images and documents using specialized forensic tools. This data can provide critical evidence regarding the author, geographic location (GPS), and the specific hardware used to create the file.

## Tools Used
* **ExifTool:** For comprehensive metadata extraction from images.[ExifTool](https://exiftool.org/)
* **PDFinfo:** For analyzing PDF document properties and versioning.[PDFinfO](https://poppler.freedesktop.org/)

## Methodology
1. **Selection:** Identified a suspicious image (`evidence.jpg`) and a document (`report.pdf`) from the disk image.
2. **Image Analysis:** Ran `exiftool evidence.jpg` to retrieve Exchangeable Image File Format (EXIF) data.
3. **Document Analysis:** Used `pdfinfo` to check for "hidden" authors and software used for PDF creation.
4. **GPS Mapping:** Extracted latitude and longitude coordinates and converted them to a readable format to identify the physical location where the photo was taken.

## Results
- **Location Found:** Successfully extracted GPS coordinates from the JPG file.
- **Author Identity:** Identified the original creator of the PDF document despite the filename being changed.
