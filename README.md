# Paarth Trade Solutions — Corporate Website

**Live Site:** [https://paarthtradesolutions.com](https://paarthtradesolutions.com)  
**Repository:** [paarthtradesolutions.github.io](https://github.com/ritikapaarth/paarthtradesolutions.github.io)  
**Platform:** GitHub Pages (static HTML/CSS/JS)

> *Global Sourcing. Trusted Distribution.*

---

## Table of Contents

1. [Overview](#overview)
2. [Repository Structure](#repository-structure)
3. [Pages](#pages)
4. [How to Update Content](#how-to-update-content)
5. [How to Add Products/Services](#how-to-add-productsservices)
6. [How to Deploy Updates](#how-to-deploy-updates)
7. [Domain & DNS Configuration](#domain--dns-configuration)
8. [Contact Form Setup (Formspree)](#contact-form-setup-formspree)
9. [SEO & Performance](#seo--performance)
10. [Branding & Design](#branding--design)
11. [Future Enhancements (Phase 2)](#future-enhancements-phase-2)

---

## Overview

Paarth Trade Solutions is a global import-export company specializing in pharmaceutical APIs, industrial raw materials, and bulk commodities. This repository hosts the corporate website — a fully static, responsive, SEO-friendly site deployed via GitHub Pages.

**Tech Stack:**
- Pure HTML5, CSS3, minimal vanilla JavaScript
- Google Fonts (Inter)
- Formspree for contact form email delivery
- GitHub Pages for hosting with HTTPS

---

## Repository Structure

```
paarthtradesolutions.github.io/
├── index.html              # Home page
├── about.html              # About Us page
├── products.html           # Products & Services page
├── markets.html            # Global Markets page
├── compliance.html         # Compliance & Quality page
├── contact.html            # Contact page with inquiry form
├── css/
│   └── style.css           # Main stylesheet (all styles)
├── js/
│   └── main.js             # Navigation, animations, scroll behavior
├── images/
│   ├── favicon.svg         # SVG favicon (convert to .ico for browser support)
│   └── hero-pattern.svg    # Hero section background pattern
├── sitemap.xml             # XML sitemap for search engines
├── robots.txt              # Search engine crawling rules
├── CNAME                   # Custom domain configuration
└── README.md               # This file
```

---

## Pages

| Page | File | Description |
|------|------|-------------|
| **Home** | `index.html` | Hero section, key services, stats bar, CTA |
| **About Us** | `about.html` | Company overview, vision/mission, leadership, core values, timeline |
| **Products & Services** | `products.html` | Pharmaceutical APIs, industrial chemicals, bulk materials, services grid, product categories table |
| **Markets** | `markets.html` | Global map visualization, Asia/Europe/USA/Global region cards, trade capabilities |
| **Compliance & Quality** | `compliance.html` | GMP, GDP, REACH, FDA frameworks, quality process, certifications |
| **Contact** | `contact.html` | Inquiry form (Formspree), contact details, business hours |

---

## How to Update Content

### Editing Text Content

1. Open the relevant `.html` file
2. Find the section you want to edit (sections are clearly marked with HTML comments like `<!-- ==================== SECTION NAME ==================== -->`)
3. Edit the text between HTML tags
4. Save and commit

### Replacing Images

1. Add your image to the `images/` folder
2. In the HTML file, find the placeholder comment (e.g., `<!-- Replace with: <img src="images/your-image.jpg" alt="Description"> -->`)
3. Replace the emoji/placeholder with an `<img>` tag:
   ```html
   <img src="images/your-image.jpg" alt="Descriptive alt text">
   ```
4. Optimize images before uploading (recommended: WebP format, max 200KB per image)

### Updating the Logo

1. Replace the SVG logo in the `<a class="logo">` element in each HTML file's header and footer
2. Or add an image logo: `<img src="images/logo.png" alt="Paarth Trade Solutions Logo">`
3. The logo appears in both the header `<nav>` and the `<footer>` — update both

### Changing Colors

All colors are defined in `css/style.css`. Key color variables:
- **Dark Blue (primary):** `#0B1D3A`
- **Accent Blue:** `#1A5276`
- **Gold Accent:** `#C9A84C`
- **Light Grey (backgrounds):** `#F4F6F9`
- **Text Color:** `#2C3E50`
- **Light Text:** `#5D6D7E`

---

## How to Add Products/Services

### Adding a New Product Category

1. Open `products.html`
2. Find the product categories table (`<table class="product-table">`)
3. Add a new row:
   ```html
   <tr>
     <td>New Category Name</td>
     <td>Example Product 1, Example Product 2</td>
     <td>Application description</td>
   </tr>
   ```

### Adding a New Service Card

1. Open `products.html`
2. Find the services card grid (`id="services"`)
3. Add a new card:
   ```html
   <div class="card fade-in">
     <div class="card-icon">&#ICON_CODE;</div>
     <h3>Service Name</h3>
     <p>Service description goes here.</p>
   </div>
   ```

### Adding a New Page

1. Copy any existing page (e.g., `products.html`) as a template
2. Update the `<title>`, meta tags, page header, and content
3. Add a link in the navigation (`nav-links`) across ALL pages
4. Add the page to `sitemap.xml`

---

## How to Deploy Updates

### Standard Deployment

1. Make your changes to the HTML/CSS/JS files
2. Commit and push to the `main` branch:
   ```bash
   git add .
   git commit -m "Update: description of changes"
   git push origin main
   ```
3. GitHub Pages will automatically deploy within 1-2 minutes
4. Verify changes at [https://paarthtradesolutions.com](https://paarthtradesolutions.com)

### Checking Deployment Status

1. Go to the repository on GitHub
2. Click **Settings** → **Pages**
3. Check the deployment status under "Your site is live at..."

---

## Domain & DNS Configuration

### Current Setup

- **Custom Domain:** `paarthtradesolutions.com`
- **CNAME File:** Contains `paarthtradesolutions.com`
- **HTTPS:** Enabled via GitHub Pages

### DNS Records (set at your domain registrar)

**Option A — A Records (recommended for apex domain):**

| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**Option B — CNAME (for www subdomain):**

| Type | Name | Value |
|------|------|-------|
| CNAME | www | paarthtradesolutions.github.io |

**Recommended: Set up both** — A records for `paarthtradesolutions.com` and a CNAME for `www.paarthtradesolutions.com`.

### Enabling HTTPS

1. Go to GitHub repository → **Settings** → **Pages**
2. Under "Custom domain", enter `paarthtradesolutions.com`
3. Check **Enforce HTTPS** (may take up to 24 hours after DNS propagation)

### Troubleshooting DNS

- DNS changes can take 24-48 hours to propagate
- Use [https://dnschecker.org](https://dnschecker.org) to verify DNS propagation
- The `CNAME` file in the repository root must contain exactly: `paarthtradesolutions.com`

---

## Contact Form Setup (Formspree)

The contact form uses [Formspree](https://formspree.io) for email delivery.

### Setup Steps

1. Go to [https://formspree.io](https://formspree.io) and create a free account
2. Create a new form — select "Email" as the notification method
3. Set the notification email to: `viswateja@paarthtradesolutions.com`
4. Copy your form endpoint (e.g., `https://formspree.io/f/xabcdefg`)
5. Open `contact.html` and replace `YOUR_FORMSPREE_ENDPOINT` in the form action:
   ```html
   <form action="https://formspree.io/f/YOUR_ACTUAL_ENDPOINT" method="POST">
   ```
6. Test the form by submitting a test inquiry

### Form Fields

| Field | Type | Required |
|-------|------|----------|
| Full Name | Text | Yes |
| Company Name | Text | Yes |
| Email Address | Email | Yes |
| Country | Text | Yes |
| Product Interest | Dropdown | No |
| Message | Textarea | Yes |

### Spam Prevention

- The form includes a honeypot field (`_gotcha`) that catches bots
- Formspree also provides built-in spam filtering

---

## SEO & Performance

### Implemented

- [x] Semantic HTML5 structure
- [x] Meta descriptions on all pages
- [x] Open Graph tags for social sharing
- [x] `sitemap.xml` for search engines
- [x] `robots.txt` allowing all crawlers
- [x] Mobile-responsive design (desktop, tablet, mobile)
- [x] Fast loading (no heavy frameworks, minimal JS)
- [x] HTTPS enabled
- [x] Clean URL structure

### Optional: Google Analytics

To add Google Analytics, insert this snippet in the `<head>` of each HTML page (before `</head>`):

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

Replace `G-XXXXXXXXXX` with your actual Google Analytics Measurement ID.

### Optional: Google Search Console

1. Go to [Google Search Console](https://search.google.com/search-console)
2. Add `paarthtradesolutions.com` as a property
3. Verify ownership via DNS TXT record
4. Submit `sitemap.xml` URL: `https://paarthtradesolutions.com/sitemap.xml`

---

## Branding & Design

| Element | Value |
|---------|-------|
| **Tagline** | Global Sourcing. Trusted Distribution. |
| **Primary Color** | #0B1D3A (Dark Blue) |
| **Accent Color** | #1A5276 (Blue) |
| **Gold Accent** | #C9A84C |
| **Background** | #F4F6F9 (Light Grey) |
| **Font** | Inter (Google Fonts) |
| **Tone** | Professional, B2B, trust-oriented |

### Favicon

The repository includes an SVG favicon (`images/favicon.svg`). For full browser compatibility:

1. Convert the SVG to `.ico` using [RealFaviconGenerator](https://realfavicongenerator.net/)
2. Place generated files in the `images/` folder
3. Update the `<link rel="icon">` tags in each HTML file

---

## Future Enhancements (Phase 2)

- [ ] Product catalog pages with downloadable PDFs
- [ ] Multi-language support (EN/DE)
- [ ] Partner login area
- [ ] Trade documentation request system
- [ ] Interactive supply chain visualization
- [ ] Blog / Industry insights section
- [ ] Client testimonials
- [ ] WhatsApp chat widget integration
- [ ] Cookie consent banner (for EU compliance)

---

## Disclaimer

> Products supplied subject to regulatory approvals in respective jurisdictions.

---

## License

© 2026 Paarth Trade Solutions. All rights reserved.

---

**Contact:** [viswateja@paarthtradesolutions.com](mailto:viswateja@paarthtradesolutions.com)
