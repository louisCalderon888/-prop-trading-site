# Walkthrough: Prop Trading Affiliate Site

## 🎯 Goal
Build a bilingual (EN/ES), AEO-optimized promotional website for prop trading firms (Apex, TopStep, etc.) using Astro and Tailwind CSS.

## 🏗️ What Was Built

### 1. Bilingual Architecture (i18n)
- **English (Default)**: `/`
- **Spanish**: `/es/`
- **Smart Header**: Automatically detects language and links efficiently.

### 2. Core Pages
| Page | Logic | Description |
|------|-------|-------------|
| **Home** | `index.astro` | Uses PAS framework copy. Hero section with active coupons. |
| **Directory** | `prop-firms/` | Lists all 24 firms from `src/data/propfirms.json`. |
| **Firm Details** | `[slug].astro` | Dynamic pages (e.g., `/prop-firms/apex`) with deep details. |
| **Comparisons** | `[firms].astro` | **Programmatic SEO**. Generates `apex-vs-topstep` automatically. |
| **Coupons** | `promo-codes.astro` | Dedicated list for discount hunters. |
| **Legal** | `privacy`, `terms` | Compliance pages including CFTC disclaimers. |

### 3. AEO (Answer Engine Optimization)
We optimized for ChatGPT/Perplexity/Claude:
- **`llms.txt`**: A map for AI bots to understand the site structure.
- **`robots.txt`**: Explicitly invites AI crawlers.
- **Schema.org**:
  - `FAQPage` on Home and FAQ pages.
  - `Product` on Firm pages.
  - `Organization` and `Offer` markup.

## 🧪 How to Verify

### 1. Build Verification
Ran `npm run build` which generated **123 static pages**.
```bash
[build] 123 page(s) built in 4.58s
[build] Complete!
```

### 2. Manual Test (Localhost)
1. Run `npm run dev`.
2. Visit `http://localhost:4321`.
3. Test Navigation:
   - Click "View All Promo Codes".
   - Switch language to "ES" (Check URL becomes `/es/promo-codes`).
   - Click a Prop Firm card (e.g., Apex).
   - Check the "Copy" button on the coupon.

### 3. Comparison Engine
Visit `http://localhost:4321/compare/apex-vs-topstep`.
- Verify the table shows side-by-side data.
- Verify "Our Take" recommendation logic is visible.

## 🚀 Deployment Status
- **GitHub**: Code pushed to `https://github.com/louisCalderon888/-prop-trading-site`.
- **Vercel**: Ready for import. No special configuration needed (Astro preset).

## ⏭️ Next Steps (Post-Launch)
1. **Connect Domain**: Set up `prop.louiscalderon.dev` in Vercel.
2. **Scraping**: When ready, implement the FireCrawl script to auto-update `propfirms.json`.
