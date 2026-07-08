# Cardstock — Digital Business Card Studio

A single-page web app for designing and exporting digital business cards. Choose from multiple templates, customize colors, add your photo, and export at print-ready resolution.

## Features

- **5 unique templates** — Linen, Obsidian, Kraft, Blueprint, and Neon
- **Real-time preview** as you type
- **Photo upload** with centered initials fallback
- **Contact fields** — email, phone, website, location
- **Social links** — LinkedIn, X/Twitter, Instagram, GitHub, Facebook, YouTube, Dribbble, TikTok, Behance
- **Accent color control** per template
- **Export at print resolution** — 3.5 × 2 in (standard business card size) at 300 dpi
- **PNG and PDF output** — PDFs include clickable social links

## Getting started

No build step or dependencies required. Just open the file:

```bash
open index.html
```

Or serve it locally:

```bash
npx serve .
```

## How it works

1. Fill in your details in the left panel
2. Click a template tab to switch designs
3. Pick an accent color that matches your brand
4. Hit **Download PNG** or **Download PDF** to save your card

Built with vanilla HTML, CSS, and JavaScript. Uses [html2canvas](https://html2canvas.hertzen.com/) and [jsPDF](https://parall.ax/products/jspdf/) via CDN for exports.

## Implementation

The app is a single `index.html` file containing all markup, styles, and logic. State lives in a plain JavaScript object and drives both the form inputs and the live card preview. Each template is a renderer function that returns HTML strings, which are injected into a `.card` element. Exports use `html2canvas` to rasterize the card at 3× scale for high-resolution PNG output, and `jsPDF` to place the same raster into a 3.5 × 2 in PDF canvas with overlaid link annotations for social URLs.

## Technologies Used

HTML, CSS, JavaScript, html2canvas, jsPDF

## Demo Video

[Youtube](https://youtu.be/pynyFVoquzQ)

