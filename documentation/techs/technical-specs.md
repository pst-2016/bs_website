# Technical Specifications

## Overview

Bytes Smith website is a fully static site — no backend, no build tools, no framework dependencies. Plain files served directly from the `docs/` folder.

---

## Stack

| Layer       | Technology              | Notes                                      |
|-------------|-------------------------|--------------------------------------------|
| Markup      | HTML5                   | Semantic elements (`nav`, `section`, `footer`) |
| Styling     | CSS3 (vanilla)          | Custom properties (variables), Flexbox, CSS Grid |
| Scripting   | JavaScript (vanilla ES6) | Mobile nav toggle, active link detection  |
| Fonts       | Google Fonts — Inter    | Loaded via CDN (`fonts.googleapis.com`)    |
| Icons       | Unicode emoji           | No icon library dependency                 |
| Hosting     | TBD (Netlify / Vercel / GitHub Pages) | Static file hosting, `docs/` as root |

---

## File Structure

```
bs_website/
├── docs/                  # Deployable site root
│   ├── index.html
│   ├── services.html
│   ├── about.html
│   ├── contact.html
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── main.js
│   └── images/            # (empty — reserved for future assets)
├── documentation/         # Project docs (not deployed)
│   ├── techs/
│   ├── adr/
│   ├── log/
│   └── project/
└── project/               # Progress tracking
```

---

## CSS Architecture

- Single stylesheet (`style.css`) — no preprocessor
- **CSS custom properties** defined in `:root` for colours, spacing, radius, shadow
- Layout via **CSS Grid** (service cards, footer columns, page layouts) and **Flexbox** (nav, buttons, utility rows)
- **`clamp()`** for fluid responsive typography — no media query font overrides needed
- Breakpoints: `900px` (tablet) and `640px` (mobile)
- Mobile nav implemented entirely in CSS + one JS class toggle (no library)

---

## Key Design Tokens

```css
--navy:       #0D1B2A   /* Primary dark — headings, nav, hero, footer */
--navy-mid:   #1A3550   /* CTA strip background */
--teal:       #06B6D4   /* Accent — labels, icons, hover states */
--teal-dark:  #0891B2   /* Accent hover / links */
--white:      #FFFFFF
--grey-light: #F1F5F9   /* Alternate section backgrounds */
--text:       #1E293B   /* Body text */
--text-light: #475569   /* Secondary / paragraph text */
--border:     #E2E8F0
```

---

## JavaScript

`main.js` is intentionally minimal — three responsibilities only:

1. Toggle `.open` class on hamburger button and nav links for mobile menu
2. Close mobile menu on nav link click
3. Add `.active` class to the current page's nav link based on `window.location.pathname`

No frameworks, no dependencies, no bundler required.

---

## Contact Form

Handled by **Formspree** (`https://formspree.io/f/mdapegoy`). The form POSTs directly to Formspree, which forwards submissions to `aldrich@bytes-smith.com`. No backend required. Free tier allows 50 submissions/month.

---

## Performance Notes

- No JavaScript frameworks or large libraries loaded
- Single CSS file, single JS file
- Google Fonts loaded with `rel="preconnect"` for faster DNS resolution
- No render-blocking resources beyond the font CDN call
- Images folder reserved but currently empty — use compressed WebP when adding assets
