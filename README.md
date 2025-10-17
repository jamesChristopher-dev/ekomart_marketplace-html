# Ekomart — Grocery & Marketplace HTML Template

> **Production-ready, conversion-first eCommerce HTML template for grocery stores, organic shops, online supermarkets and multi-vendor marketplaces.**
> Clean code, Bootstrap 5 foundation, RTL-ready, and crafted to convert visitors into customers.

## Project Overview

Ekomart is a premium, fully responsive HTML template built specifically for grocery eCommerce and multi-vendor marketplaces. It ships with 5 polished homepage variations, 50+ inner pages, an admin dashboard skeleton, RTL support, and all the interactive UI components a modern grocery store needs: product grids, vendor pages, quick-view, mini cart, wishlist, and promotional sections.

This repository contains the static front-end source, compiled assets (CSS/JS), screenshots and documentation that make the template production-ready and easy to integrate with any backend or CMS.

---

## One-line Pitch

Launch a high-converting grocery marketplace or single-vendor shop in days — pixel-perfect UI, Bootstrap 5 foundation, RTL-ready and optimized for performance & SEO.

---

## Screenshots

> (Add these images to your repo `assets/screenshots/` so they render on GitHub)

![Ekomart 1](https://github.com/user-attachments/assets/834d1134-c5ff-4a03-87a1-751ed54acd29)
![Ekomart 2](https://github.com/user-attachments/assets/f134ddb0-1e4d-4da2-aaef-70de0402916a)
![Ekomart 3](https://github.com/user-attachments/assets/f175f6ca-5e36-47d2-a253-984a2139247b)
![Ekomart 4](https://github.com/user-attachments/assets/2e1f0d8f-3ac0-4219-a955-9680b03a67ea)
![Ekomart 5](https://github.com/user-attachments/assets/ab3426a0-82b6-45e4-973a-fe8231a30f51)

---

## Key Features

* **5 Homepage Variations** (single-vendor, organic shop, supermarket, multi-vendor, promo layout).
* **50+ Inner Pages**: shop grids, product detail variations, vendor listings, blog, contact, checkout, invoice, account pages.
* **Vendor Management UI**: vendor grids, vendor detail pages, vendor-styled product listings.
* **Interactive eCommerce Elements**: mini cart, quick view modal, wishlist, compare, product filters with autocomplete search.
* **Promotion & Marketing Blocks**: hero banners, coupons, badges (e.g. 25% off), weekly best-sellers.
* **Admin Dashboard (static)**: sales widgets, product management pages, order tracking (dashboard/index.html).
* **RTL Support**: full RTL demo and mirrored layouts for Arabic/Hebrew markets.
* **SEO & Performance**: semantic HTML, minified assets, image optimization, critical CSS considerations.
* **Accessibility-minded**: semantic tags, ARIA attributes, keyboard-aware navigation.
* **Extensible**: convert to React/Vue, or integrate with WordPress / headless CMS.

---

## Tech Stack & Tools

* **Core:** HTML5, CSS3, Bootstrap 5
* **Styling:** SCSS (source included) → compiled CSS (minified for production)
* **Interactivity:** Vanilla JS + jQuery for legacy plugins where necessary
* **Carousels / Sliders:** Owl Carousel or Slick (included examples)
* **Icons & Fonts:** Google Fonts (e.g., Roboto/Open Sans), Font Awesome / Bootstrap Icons
* **Design Files:** Figma (prototypes used during design)
* **Optimization:** images optimized via TinyPNG / ImageMagick for distribution

---

## Development Process & Best Practices

This project followed a structured workflow:

1. **Design → Prototype:** High-fidelity designs in Figma; component library defined.
2. **Mobile-first implementation:** Bootstrap 5 utilities plus SCSS variables for robust responsiveness.
3. **Modular code:** Partial HTML includes, SCSS components and modular JS files to keep scope isolated and maintainable.
4. **Accessibility:** ARIA attributes, keyboard support for menus/modals and color contrast checks.
5. **Performance first:** Lazy-loading, minified assets, optimized images, and critical CSS.
6. **Versioning:** Git with feature branches and clear commits (feature/admin-dashboard etc.).

---

## How to run locally (copy & paste)

No build system is required to preview — template is static.

```bash
# Clone your repository (replace URL accordingly)
git clone https://github.com/your-username/ekomart-template.git
cd ekomart-template

# Quick preview with Live Server (VS Code) OR using a tiny static server
# Option A (VS Code Live Server): open project and start Live Server extension
# Option B (npm http-server)
npm install -g http-server
http-server -c-1 . -p 8080

# Open http://localhost:8080 in your browser
```

---

## Recommended Build / Dev Scripts

If you want a small Node toolchain for compiling SCSS, autoprefixing, and optimizing assets, use this example `package.json` scripts (optional):

```json
"scripts": {
  "dev": "npx http-server -c-1 . -p 8080",
  "sass": "sass --watch assets/scss:assets/css --style=expanded",
  "build:css": "sass assets/scss:assets/css --style=compressed && postcss assets/css/*.css --use autoprefixer -d assets/css",
  "optimize:images": "imagemin assets/images/* --out-dir=dist/images",
  "build": "npm run build:css && npm run optimize:images"
}
```

---

## Integration & Back-end Suggestions

Ekomart is purposely backend-agnostic. Integration options:

* **PHP / Laravel**

  * Use Laravel routes + Blade components to replace HTML includes with dynamic templates.
  * Build APIs for cart, checkout and vendors; connect via AJAX/fetch.

* **Node.js / Express**

  * Serve templates and expose REST endpoints for products, carts and orders.
  * Use server-side rendering or headless approach with a frontend SPA.

* **Headless / Jamstack**

  * Export product data from a headless CMS (Strapi / Sanity) and generate static site or use a small client-side JS to fetch data.
  * Deploy to Netlify or Vercel with serverless functions for checkout.

* **WordPress (if preferred)**

  * Convert templates into WordPress theme files or use as theme HTML for WooCommerce storefront.

**Data flows to implement**: product catalog API, cart/session persistence, checkout/payment webhooks (Stripe/PayPal), vendor management endpoints.

---

## Admin Panel (Included) & Wiring to API

A static admin dashboard is included (`dashboard/index.html`) and simulates the typical admin experience:

* Sales widgets, charts (chart placeholders), products table, order details and vendor approvals.

**To make it dynamic:**

* Replace static tables with calls to `/api/orders`, `/api/products`, `/api/vendors`.
* Use a simple JWT-protected API and fetch data via `fetch()` or Axios.
* For charts, plug Chart.js with server-provided time series.

---

## Customization Guide (fast wins)

* **Brand colors & fonts**: update `assets/scss/_variables.scss` and recompile.
* **Hero & banners**: swap hero backgrounds and calls-to-action per promotion.
* **Product cards**: edit templates in `components/` to change badges, add vendor chips or delivery ETA.
* **RTL**: use `dir="rtl"` and the provided RTL CSS to flip layout — test important pages after switching.
* **Image pipeline**: replace demo images, then run image optimization pipeline (WebP recommended).

---

## Performance, SEO & Accessibility

* **Performance**

  * Use WebP images with `srcset` and `sizes`.
  * Lazy-load below-the-fold images (`loading="lazy"`).
  * Minify JS/CSS for production builds.
* **SEO**

  * Correct meta tags, Open Graph, canonical links and structured data for products (`Product` schema).
  * Use semantic markup (`<main>`, `<article>`, `<nav>`).
* **Accessibility**

  * Keyboard-focusable nav & modal controls.
  * Adequate contrast for CTAs and badges.
  * Add `alt` attributes to images and ARIA labels for dynamic controls.

---

## Testing & QA Checklist

* Cross-browser testing: Chrome, Firefox, Safari, Edge (use BrowserStack).
* Mobile devices: iOS Safari, Android Chrome on multiple screen sizes.
* Checkout flows: simulate order creation, promo code application and error cases.
* RTL: verify mirrored layout, form alignment, input caret placement and icons.
* Performance regression testing: Lighthouse audits pre/post changes.

---

## Deployment & CI/CD (recommended)

* **Static / Front-end hosting**: Netlify, Vercel, GitHub Pages or S3 + CloudFront.
* **CI**: GitHub Actions to run linting, build SCSS and deploy `dist/` folder to your host.
* **Example GitHub Actions steps**:

  * `checkout` → `npm ci` → `npm run build` → deploy to Netlify/Vercel or push `dist/` to S3.

---

## Suggested File Structure

```
/ (root)
├─ index.html
├─ home-2.html
├─ home-3.html
├─ shop/
│  ├─ shop-grid.html
│  └─ product-single.html
├─ dashboard/
│  └─ index.html
├─ assets/
│  ├─ css/
│  ├─ scss/
│  ├─ js/
│  └─ images/
├─ docs/
│  └─ README.md
└─ LICENSE
```

---

## How to pitch this to clients / recruiters

**Client pitch (short):**
“Ekomart is a ready-to-launch grocery marketplace template designed to convert — mobile-first, SEO-optimized and extensible to multi-vendor platforms. Launch your MVP quickly and validate revenue streams (subscriptions, vendor commissions, promotions).”

**Recruiter bullets to highlight in interviews**

* Responsible for end-to-end front-end delivery: Figma → implementation → performance tuning.
* Built modular SCSS, semantic HTML and accessible components (WCAG-aware).
* Implemented RTL and multi-vendor UX patterns — important for international markets.
* Demonstrated measurable performance improvements (90+ Lighthouse target) via image optimization and critical CSS.

---

## Roadmap / Next Improvements

* React/Vue component library conversion (Headless & dynamic).
* Payment & cart demo wiring (Stripe sandbox integration).
* Small vendor admin (dynamic) with authentication.
* Visual regression tests and automated Lighthouse scoring in CI.
* Headless ecommerce example (Strapi / Sanity + static generation).

---

## Support & Contact

**Author / Maintainer:** Your Name

* Portfolio / Contact: `https://your-portfolio.example.com`
* Email: `your.email@example.com`
  *(Replace placeholders with your real contact info.)*

Support policy: lifetime free updates for template bugfixes; response time within 24–48 hours for support requests.

---

## License

This template is released under **[MIT License]** (or replace with your preferred license). See `LICENSE` file for details.
