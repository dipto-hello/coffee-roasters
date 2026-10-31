# ☕ Coffee Roasters & Cafe

[![Live Site](https://img.shields.io/badge/Live_Site-GitHub_Pages-blue?style=for-the-badge&logo=github)](https://diptohello.me/coffee-roasters/)
[![Edge Deployment](https://img.shields.io/badge/Edge_Mirror-Cloudflare_Workers-orange?style=for-the-badge&logo=cloudflare)](https://velvet-brew.sarkerdipto107.workers.dev/)
[![Stack](https://img.shields.io/badge/Stack-Vanilla_JS_%7C_Canvas-yellow?style=for-the-badge&logo=javascript)](https://diptohello.me/coffee-roasters/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

A web platform built for **Coffee Roasters & Cafe**, located on Road 11, Banani, Dhaka. The site pairs a smooth HTML5 Canvas scrollytelling introduction with an interactive seasonal menu, takeaway ordering cart, and table reservation flow.

---

## 🔗 Live Deployments

* **Primary Website:** [diptohello.me/coffee-roasters](https://diptohello.me/coffee-roasters/) (GitHub Pages Mirror)
* **Cloudflare Workers Mirror:** [velvet-brew.sarkerdipto107.workers.dev](https://velvet-brew.sarkerdipto107.workers.dev/)

---

## ☕ What's Inside

### 1. Canvas-Based Scrollytelling
* Uses native window scrolling rather than scroll-jacking, keeping trackpad and touch interactions natural.
* Renders transitions between key photography frames using an independent `requestAnimationFrame` loop on an HTML5 `<canvas>`.
* Responsive framing maintains subject focal points across mobile screens and wide desktop monitors.

### 2. Seasonal Food & Beverage Menu
* Filter items across categories: Specialty Coffee, Artisan Bakery, Breakfast & Lunch, and Desserts.
* Filter by dietary tags including Vegan, Gluten-Free, and Chef's Pick.
* Live item pricing in Bangladeshi Taka (BDT) with clear ingredient breakdowns.

### 3. Takeaway Cart & Order Flow
* Slide-out cart drawer tracking item counts, customizations, subtotal, and estimated tax.
* Interactive toast notifications confirming items added, updated, or removed.

### 4. Table Reservation
* Accessible modal built using the native HTML `<dialog>` element.
* Supports keyboard navigation, `Escape` key dismissal, backdrop clicks, and basic form validation.

### 5. Media Pipeline & Performance
* 22 high-resolution imagery assets converted to WebP format, cutting file sizes by roughly 50% without visible quality loss.
* Critical above-the-fold assets preloaded via `<link rel="preload">` to speed up initial paint times.
* Below-the-fold images use native `<picture>` tags with lazy loading.

### 6. Search & Social Sharing
* OpenGraph and Twitter Card metadata for social previews on WhatsApp, Facebook, LinkedIn, and X.
* Schema.org `CafeOrCoffeeShop` structured data (JSON-LD) with location coordinates for Banani, Dhaka.

---

## 📁 Directory Structure

```text
artisan-cafe/
├── assets/
│   └── images/            # WebP and JPEG photography (Coffee, Food, Interior)
├── docs/                  # Design specs and architectural blueprints
├── scripts/
│   └── convert-webp.js    # Node.js batch image conversion utility
├── src/
│   ├── app.js             # Cart management, reservation dialog, and menu filters
│   ├── menu-data.js       # Food and drink item catalog with pricing
│   └── scrolly-cinema.js  # Canvas scroll interpolation engine
├── styles/
│   ├── main.css           # Global layout, color palette, and component styles
│   └── scrolly-cinema.css # Canvas viewport and chapter telemetry styling
├── index.html             # Main entry point with OpenGraph and structured data
├── server.js              # Minimal zero-dependency local HTTP preview server
├── audit-test.mjs         # End-to-end integration test suite
└── README.md              # Project documentation
```

---

## 🛠️ Local Development

To run the project locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dipto-hello/coffee-roasters.git
   cd coffee-roasters
   ```

2. **Start the local server:**
   ```bash
   node server.js
   ```

3. **Open the browser:**
   ```text
   http://localhost:3000
   ```

---

## 🧪 Running Tests

Run the built-in audit test suite:

```bash
node audit-test.mjs
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
