# Smith Plumbing Website

## Overview
A brochure website for Smith Plumbing, a Manchester-based plumbing company established in 2005.

## Tech Stack
- **Framework**: Astro 5
- **Styling**: Tailwind CSS 4 (via `@tailwindcss/vite` plugin)
- **Language**: TypeScript
- **Package manager**: npm

## Commands
- `npm run dev` — Start dev server
- `npm run build` — Build for production (output in `dist/`)
- `npm run preview` — Preview production build locally

## Project Structure
```
src/
├── site.config.ts        # Central site config (name, contact info, nav links)
├── assets/               # SVG assets
├── components/
│   ├── Nav.astro         # Navigation component
│   ├── Footer.astro      # Footer component
│   └── CtaBanner.astro   # Reusable CTA banner (dark bg, call + quote buttons)
├── layouts/
│   └── Layout.astro      # Shared page layout wrapper
├── pages/
│   ├── index.astro       # Homepage (Hero → Services → Why Choose Us → CTA Banner → Areas)
│   ├── about.astro       # About page (Hero → Story → Values → Team → Accreditations → CTA)
│   ├── areas.astro       # Areas page (Hero → Area Cards Grid → Not Listed Here? → CTA)
│   ├── contact.astro     # Contact page (Hero → Form + Details → FAQ accordion → CTA)
│   ├── services.astro    # Services page (Hero → 6 alternating service sections → CTA)
│   └── 404.astro         # Custom 404 page
└── styles/
    └── global.css        # Global styles
```

## SEO
- **Sitemap**: Auto-generated via `@astrojs/sitemap` integration
- **robots.txt**: In `public/robots.txt`, allows all crawlers
- **JSON-LD**: LocalBusiness schema injected via Layout component
- **Open Graph**: og:title, og:description, og:type, og:url on every page
- **Meta descriptions**: Unique per page, passed via Layout props
- **Favicon**: Custom SVG (blue circle + wrench) in `public/favicon.svg`

## Key Conventions
- Site-wide settings (business name, phone, email, address, nav links) live in `src/site.config.ts`
- All pages use the shared `Layout.astro` wrapper
- Tailwind CSS is configured through the Vite plugin in `astro.config.mjs`
- `address` in site config is an object — use `siteConfig.address.full` for display

## Business Details
- **Name**: Smith Plumbing
- **Location**: 45 Deansgate, Manchester, M3 2AY
- **Phone**: 0161 555 0199
- **Email**: info@smithplumbing.co.uk
- **Website**: https://smith-plumbing.netlify.app
