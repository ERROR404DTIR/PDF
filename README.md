# PDF — Browser-based PDF editor

A lightweight, privacy-first PDF workspace. Open a PDF, add annotations and visual elements, then export the edited document. Everything runs in your browser; files are not uploaded to an application server.

## Features

- Open and preview multi-page PDF files
- Page thumbnails and page navigation
- Add text annotations and adjust their content, size, and color
- Add images (PNG, JPG, WebP)
- Freehand drawing
- Add rectangles, highlights, and white cover areas
- Select, move, resize, duplicate, and delete added elements
- Undo and redo
- Zoom and export the modified PDF
- Responsive layout for desktop and mobile

## Important editing limitation

This version adds editable overlay elements to the PDF. It does **not** rewrite the original embedded text objects or reconstruct the source document's fonts and layout. To visually replace existing text, place a white cover over it and add a new text annotation. A cover is a visual overlay, not a secure redaction; do not use it to conceal sensitive information.

## Run locally

No build step is required. Open `index.html` through a local static server (recommended):

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

The app loads PDF.js and pdf-lib from public CDNs, so an internet connection is required to load those libraries. Your selected PDF itself is processed locally in the browser.

## Privacy

The application does not upload document contents to a backend. Avoid using shared or public devices for confidential documents. Browser extensions and the hosting/CDN providers are outside this project's control.

## License

MIT
