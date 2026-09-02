
# 📄 PDFify

A clean, client-side web app that converts files to PDF — entirely in your browser. No backend, no file uploads to a server, no privacy concerns. Built with plain HTML, CSS, and JavaScript.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)

<img width="720" height="973" alt="roy" src="https://github.com/user-attachments/assets/b914ec56-ef17-47a1-9d6b-6c900d6cfb44" />


## -- Features

- **🖼️ Image → PDF** — Convert JPG, PNG, WEBP, and GIF files into a PDF document
- **📝 Text → PDF** — Convert plain `.txt` files into a formatted PDF
- **🖱️ Drag & drop** — Drop files directly onto the page, or use the file picker
- **🌗 Dark mode** — Toggle between light and dark themes
- **🌐 Arabic translation** — Full UI translation with automatic RTL layout switch
- **🔒 100% private** — All conversion happens locally in the browser; files never leave the user's device
- **⚡ No installation** — A single `index.html` file, works instantly with no build step

## 🛠️ Tech Stack

- HTML5 / CSS3 (custom properties for theming)
- Vanilla JavaScript (no framework)
- [jsPDF](https://github.com/parallax/jsPDF) (via CDN) for PDF generation
- Google Fonts: Plus Jakarta Sans (English) & Cairo (Arabic)

## 🚀 Getting Started

### Run locally
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/pdfify.git
   cd pdfify
   ```
2. Open `index.html` directly in your browser, **or** use the VS Code "Live Server" extension for auto-reload during development.

No `npm install`, no build tools, no server required.

### Deploy
Since this is a fully static site, you can host it for free on:
- [GitHub Pages](https://pages.github.com/)
- [Netlify](https://www.netlify.com/)
- [Vercel](https://vercel.com/)

## 📁 Project Structure

```
pdfify/
├── index.html      # Everything: markup, styles, and logic in one file
└── README.md
```

## 📌 Current Limitations

| File type | Supported? |
|---|---|
| Images (JPG, PNG, WEBP, GIF) | ✅ Yes |
| Plain text (.txt) | ✅ Yes |
| Word (.docx) | ❌ Not yet |
| Excel (.xlsx) | ❌ Not yet |
| PowerPoint (.pptx) | ❌ Not yet |
| PDF → Image (reverse) | ❌ Not yet |

Office file formats (Word/Excel/PowerPoint) can't be reliably converted with client-side JavaScript alone — they require a backend service (e.g. LibreOffice headless) to render accurately.

## 🗺️ Roadmap / Future Improvements

- [ ] **Backend support for Office files** — Add a Node.js/Python backend (e.g. using LibreOffice headless or a conversion API) to support `.docx`, `.xlsx`, and `.pptx`
- [ ] **Merge multiple images into one PDF page layout** — Options for grid/collage layouts, not just one image per page
- [ ] **PDF compression/quality settings** — Let users choose output quality vs. file size
- [ ] **Reordering files before conversion** — Drag-to-reorder the file list so pages appear in the desired order
- [ ] **PDF → Image / PDF → Text** — Support the reverse conversion direction
- [ ] **Page size & orientation options** — Let users pick A4/Letter, portrait/landscape
- [ ] **Progress bar for large files** — Visual feedback during conversion of large batches
- [ ] **More languages** — Extend the translation system (`translations` object in the JS) beyond English/Arabic
- [ ] **PWA support** — Make the app installable and usable offline
- [ ] **Unit tests** — Add basic tests for the conversion logic
- [ ] **Accessibility pass** — Full keyboard navigation and screen-reader labeling audit

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to fork the project and submit a pull request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

youcef.m

