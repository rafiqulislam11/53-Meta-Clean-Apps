# 53-Meta-Clean-Apps (MetaClean Studio)

> **100% Zero-Trace Forensic Image Metadata & EXIF Scrubber**  
> Complete client-side privacy tool to permanently strip EXIF, GPS location coordinates, camera models, lens serials, Adobe XMP packets, and IPTC tags from bulk photos.

---

## 🛡️ 100% Forensic Cleaning Guarantee

Standard metadata strippers often leave embedded ICC color profiles, PNG text chunks, or proprietary camera markers behind. **MetaClean Studio** applies a **Dual-Layer Forensic Pipeline**:

1. **Layer 1: Offscreen Pixel Canvas Decoupling**  
   Decodes the raw RGBA pixel raster directly into memory, completely separating the image pixels from the original file container and discarding all original metadata headers.

2. **Layer 2: Raw Binary Marker Purge**  
   Directly parses and sanitizes the exported binary bitstream byte-by-byte:
   - **JPEG**: Permanently purges all `APP1` through `APP15` segments (`0xFFE1`–`0xFFEF`) and `COM` comment markers (`0xFFFE`). Retains only clean structural markers (`SOI`, clean `APP0`, `DQT`, `DHT`, `SOF`, `SOS`, `EOI`).
   - **PNG**: Strips all non-critical chunks (`eXIf`, `tEXt`, `zTXt`, `iTXt`, `tIME`, `iCCP`, `pHYs`). Retains only essential chunks (`IHDR`, `IDAT`, `PLTE`, `tRNS`, `IEND`).
   - **WebP**: Purges `EXIF`, `XMP `, and `ICCP` chunks from RIFF containers.

---

## ✨ Features

- **📍 Complete Geotag Removal**: Eliminates GPS Latitude, Longitude, Altitude, and Timestamp data.
- **📷 Device Fingerprint Wiped**: Removes Camera Make, Model, Lens Serial Numbers, Shutter counts, and ISO parameters.
- **🕒 Timestamp & History Scrub**: Wipes capture dates, modification timestamps, and Adobe Photoshop/Lightroom editing history.
- **👁️ Forensic Audit Inspector**: Click on any image to inspect the **Before vs. After** forensic comparison report.
- **🔒 Filename Anonymization**: Automatically renames files (e.g. `clean_image_01.jpg`) so original device filenames like `IMG_20261007_iPhone15.jpg` don't leak information.
- **📦 In-Browser Batch ZIP Export**: Download all sanitized images bundled into a single ZIP file created 100% offline.
- **⚡ Zero Server Uploads**: 100% client-side execution in your browser using the HTML5 Canvas & TypedArray APIs.

---

## 🚀 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/rafiqulislam11/53-Meta-Clean-Apps.git
   ```
2. Double-click **`index.html`** to open it directly in any modern web browser (Google Chrome, Microsoft Edge, Firefox, Brave, Safari).
3. Drag & drop images or click **"Select Images"** / **"⚡ Try Demo Images"** to test immediately.
