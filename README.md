# 53-Meta-Clean-Apps (MetaClean Studio)

> **100% Universal Forensic Metadata Scrubber**  
> Complete zero-trace metadata cleaner for **EPS (PostScript)**, **AI (Adobe Illustrator)**, **SVG (Vector)**, **JPEG / JPG**, **PNG**, **WebP**, **PDF**, and **GIF/BMP**.

---

## 🎨 Supported Formats & Cleaning Engines

### 1. ⚡ EPS (`.eps` - Encapsulated PostScript)
- **Adobe XMP Packets**: Strips `%begin_xml_packet:` to `%end_xml_packet:` and `<?xpacket?>` XML blocks.
- **DSC Header Scrubbing**: Sanitizes `%%Creator:` (software tool), `%%For:` (licensed user/designer name), `%%CreationDate:`, `%%Title:`, `%%Copyright:`, and routing comments.
- **Vector Integrity**: Retains paths, bezier curves, fills, strokes, colors, and bounding boxes (`%%BoundingBox`) 100% valid.

### 2. 🎨 AI (`.ai` - Adobe Illustrator Artwork)
- **PDF Info Dictionary Purge**: Wipes `/Author`, `/Creator`, `/Producer`, `/CreationDate`, `/ModDate`, `/Title`, and `/Subject`.
- **Adobe XMP Streams**: Neutralizes embedded `<x:xmpmeta>` streams and Photoshop/Illustrator history packets.
- **Document Tracking ID**: Removes unique UUIDs and `/ID [<...><...>]` tracking tokens.
- **Artboard & Vector Preservation**: All layers, artboards, and vector objects remain fully editable.

### 3. 📐 SVG (`.svg` - Scalable Vector Graphics)
- **Metadata Blocks**: Strips `<metadata>`, `<rdf:RDF>`, and Dublin Core elements (`<dc:creator>`, `<dc:date>`).
- **Editor Namespaces**: Strips Inkscape (`inkscape:version`, `sodipodi:docname`) and Adobe Illustrator private data (`<i:pgf>`).
- **Comments & Descriptions**: Strips XML comments (`<!-- ... -->`), `<title>`, and `<desc>` tags.

### 4. 📷 Raster Images (JPEG, PNG, WebP)
- **Dual-Layer Pipeline**: Canvas pixel decoupling + raw binary marker purge.
- **EXIF 2.3 & Geotags**: Strips GPS Latitude/Longitude/Altitude coordinates, camera models, lens serial numbers.
- **ICC & IPTC**: Strips ICC device color profiles and IPTC copyright information.
- **PNG Chunks**: Strips `eXIf`, `tEXt`, `zTXt`, `iTXt`, `tIME`, and `pHYs`.

---

## ✨ Features

- **100% In-Browser Execution**: Zero server uploads, completely offline, zero API latency.
- **Drag & Drop / Clipboard Paste**: Drag multiple files or paste directly with `Ctrl + V`.
- **⚡ One-Click Demo Files**: Instantly test with simulated EPS, AI, SVG, and GPS JPG files.
- **Forensic Audit Inspector**: Click the eye icon on any file to view a Before vs. After metadata inspection report.
- **Batch ZIP Export**: Export all cleaned files into a single ZIP archive created in-memory.
- **Filename Anonymization**: Automatically renames outputs (e.g. `clean_eps_01.eps`, `clean_ai_01.ai`) to prevent leaking personal info from original file names.

---

## 🚀 Quick Start

1. Clone repository:
   ```bash
   git clone https://github.com/rafiqulislam11/53-Meta-Clean-Apps.git
   ```
2. Double-click **`index.html`** to run in any modern web browser.
