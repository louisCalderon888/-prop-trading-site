# Prop Trading Promo Codes Website

A specialized affiliate marketing website for prop trading firms, built with Astro, Tailwind CSS, and optimized for AEO (Answer Engine Optimization).

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 📂 Project Structure

- `src/pages/`:
  - `index.astro`: Homepage (English)
  - `es/`: Spanish version of the site
  - `prop-firms/`: Directory and dynamic firm pages (`[slug].astro`)
  - `compare/`: Programmatic comparison pages (`[firms].astro`)
  - `promo-codes.astro`: List of all active coupons
  - `ninjatrader.astro`: Platform landing page
  - `faq.astro`: Knowledge base with Schema
- `src/data/propfirms.json`: **Single source of truth** for all prop firm data.
- `src/components/`: Reusable UI components.
- `public/`: Static assets, `robots.txt`, `llms.txt`.

## 🌍 Internationalization (i18n)

The site is bilingual (EN/ES).
- English is the default path (`/`).
- Spanish is under `/es/`.
- `Header.astro` handles language switching logic.

## 🛠️ Maintenance

### Adding a New Prop Firm
1. Open `src/data/propfirms.json`.
2. Add a new object to the array following the existing schema.
3. The site will automatically generate:
   - A detail page (`/prop-firms/new-firm`)
   - Comparison pages against all other firms (`/compare/new-firm-vs-others`)
   - Directory listing
   - Coupon card

### Updating Promo Codes
Edit `src/data/propfirms.json`. Update the `code` and `discount` fields. The "Last Updated" dates on the site update automatically via JS, but for real accuracy, we will implement the FireCrawl scraper later.

## 🚢 Deployment (Vercel)

This project is optimized for Vercel.

1. Push code to GitHub.
2. Import project in Vercel.
3. Framework Preset: `Astro`.
4. Build Command: `npm run build`.
5. Output Directory: `dist`.
6. Deploy.

## 🤖 AEO Features

- **llms.txt**: Context for AI crawlers like ChatGPT.
- **Semantic HTML**: Optimized for parsing.
- **JSON-LD Schema**:
  - `FAQPage`: On FAQ and Home pages.
  - `Product`: On firm detail pages.
  - `Offer`: For coupon codes.
  - `Organization`: For firm details.

## ⚠️ Compliance

Ensure you strictly follow the **NinjaTrader Vendor Guidelines**.
- Do not make income guarantees.
- Keep the risk disclosure visible (Footer/Disclaimer page).
- Do not imply you are NinjaTrader (use "Authorized Vendor" language).
