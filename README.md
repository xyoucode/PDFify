# 📄 PDFify

**100% Private, Client-Side PDF Converter** — a clean web app that converts files to PDF entirely in your browser. No backend, no file uploads to a server, no privacy concerns. Built with plain HTML, CSS, and JavaScript.

🔗 **Live:** https://xyoucode.github.io/PDFify/

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)

<img width="720" height="973" alt="roy" src="https://github.com/user-attachments/assets/b914ec56-ef17-47a1-9d6b-6c900d6cfb44" />


##  Features

- **🖼️ Image → PDF** — Convert JPG, PNG, WEBP, and GIF files into a PDF document
- **📝 Text → PDF** — Convert plain `.txt` files into a formatted PDF, with Unicode/UTF-8 font support (accented Latin characters like é, à, ü render correctly via a dynamically-loaded Noto Sans font)
- **🖱️ Drag & drop** — Drop files directly onto the page, or use the file picker
- **🌍 8 languages** — English, French, Spanish, Portuguese, German, Chinese, Japanese, and Arabic (with automatic RTL layout for Arabic)
- **🧭 Auto language detection** — Reads the visitor's browser language (`navigator.language`) on first visit and picks a matching UI language automatically; falls back to English if unsupported
- **🌐 Language picker** — Click the globe icon to open a dropdown listing all supported languages by native name, with the active one checked — no need to cycle through them
- **💾 Remembers your choice** — Language and theme preferences are saved in `localStorage`, so returning visitors see their last setting instead of the default
- **🌗 Dark mode** — Defaults to the visitor's OS-level preference (`prefers-color-scheme`), with a manual toggle that overrides it
- **🔒 Visible privacy note** — A small lock-icon note next to the upload button reassures visitors their files are processed locally and never sent to a server
- **📱 Mobile-friendly** — Responsive layout with a hamburger menu (☰) on small screens that collapses theme/language/CTA controls into a slide-down panel
- **🖼️ Social share preview** — Custom favicon and Open Graph / Twitter Card image, so the link looks polished when shared on WhatsApp, X, Discord, etc.
- **⚡ No installation** — A single `index.html` file, works instantly with no build step

## 🛠️ Tech Stack

- HTML5 / CSS3 (custom properties for theming, no framework)
- Vanilla JavaScript (no framework, no build tools)
- [jsPDF](https://github.com/parallax/jsPDF) (via CDN) for PDF generation
- [Noto Sans](https://fonts.google.com/noto/specimen/Noto+Sans) (fetched at runtime) for Unicode text-to-PDF rendering
- Google Fonts: Plus Jakarta Sans (Latin scripts) & Cairo (Arabic)

## 🚀 Getting Started

### Run locally
1. Clone the repository:
   ```bash
   git clone https://github.com/xyoucode/PDFify.git
   cd PDFify
   ```
2. Open `index.html` directly in your browser, **or** use the VS Code "Live Server" extension for auto-reload during development.

No `npm install`, no build tools, no server required.

### Deploy
Fully static site — currently hosted for free on [GitHub Pages](https://pages.github.com/). Also works on [Netlify](https://www.netlify.com/) or [Vercel](https://vercel.com/) with zero configuration.

## 📁 Project Structure

```
PDFify/
├── index.html            # Everything: markup, styles, and logic in one file
├── favicon.png            # Tab icon
├── apple-touch-icon.png   # iOS home-screen icon
├── preview.png            # Social share preview image (Open Graph / Twitter Card)
└── README.md
```

## 📌 Current Limitations

| File type | Supported? |
|---|---|
| Images (JPG, PNG, WEBP, GIF) | ✅ Yes |
| Plain text (.txt), Latin/accented characters | ✅ Yes |
| Plain text (.txt), Arabic / Chinese / Japanese glyphs inside the PDF itself | ❌ Not yet (needs a larger embedded CJK/Arabic font) |
| Word (.docx) | ❌ Not yet |
| Excel (.xlsx) | ❌ Not yet |
| PowerPoint (.pptx) | ❌ Not yet |
| PDF → Image (reverse) | ❌ Not yet |

Office file formats (Word/Excel/PowerPoint) can't be reliably converted with client-side JavaScript alone — they require a backend service (e.g. LibreOffice headless) to render accurately.

## 🗺️ Roadmap / Future Improvements

- [ ] **Backend support for Office files** — Add a Node.js/Python backend (e.g. using LibreOffice headless or a conversion API) to support `.docx`, `.xlsx`, and `.pptx`
- [ ] **CJK & Arabic text rendering inside PDFs** — Embed a dedicated Noto Sans SC/JP/Arabic font for `.txt` conversion (larger download, currently out of scope)
- [ ] **Merge multiple images into one PDF page layout** — Options for grid/collage layouts, not just one image per page
- [ ] **PDF compression/quality settings** — Let users choose output quality vs. file size
- [ ] **Reordering files before conversion** — Drag-to-reorder the file list so pages appear in the desired order
- [ ] **PDF → Image / PDF → Text** — Support the reverse conversion direction
- [ ] **Page size & orientation options** — Let users pick A4/Letter, portrait/landscape
- [ ] **Progress bar for large files** — Visual feedback during conversion of large batches
- [ ] **PWA support** — Make the app installable and usable offline
- [ ] **Unit tests** — Add basic tests for the conversion logic
- [ ] **Accessibility pass** — Full keyboard navigation and screen-reader labeling audit
- [ ] **Possible rebrand** — Evaluating a new project name (candidates under review) since "PDFify" overlaps with existing products

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to fork the project and submit a pull request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

Built by YOUCEF.M

