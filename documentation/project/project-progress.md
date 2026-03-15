# Bytes Smith Website — Project Progress

## Done

### Planning & Documentation
- Defined company overview: three service pillars (AI Products, Custom AI Solutions, AI Services & Consultancy), Singapore base
- Created `documentation/project_overview.md` with goals, target audience, site structure, design direction, and success criteria
- Referenced [purplerhino.co.uk](https://www.purplerhino.co.uk/) for design inspiration — sectional layout, bold hero, three-column cards, honest/consultative tone

### Website Build (static HTML/CSS/JS)
- `docs/css/style.css` — full shared stylesheet: variables, typography, layout, components, responsive breakpoints
- `docs/js/main.js` — mobile nav toggle and active link highlighting
- `docs/index.html` — homepage: hero, services cards, "Why Bytes Smith" trust strip, CTA, footer
- `docs/services.html` — detailed services page with anchor links (`#products`, `#custom`, `#consultancy`)
- `docs/about.html` — company story, values grid, Singapore context
- `docs/contact.html` — contact form with service selector, contact details

---

## Next Steps

### Content
- [ ] Replace placeholder email `hello@bytessmith.com` with real contact email
- [ ] Add real company registration details (Pte. Ltd. number) to footer if needed
- [ ] Add team bios or headshots to About page (optional at launch)
- [ ] Populate AI Products section with actual product names/descriptions when ready

### Technical
- [ ] Add `favicon.ico` (and optionally `apple-touch-icon.png`) to `docs/`
- [ ] Hook up contact form to a form backend — recommended options:
  - [Formspree](https://formspree.io) — free tier, no backend needed
  - [Netlify Forms](https://docs.netlify.com/forms/setup/) — free if hosting on Netlify
- [ ] Add basic meta open graph tags (`og:title`, `og:description`, `og:image`) for link previews
- [ ] Create a simple `404.html` page

### Deployment
- [ ] Choose a hosting platform:
  - **Netlify** — drag and drop `docs/` folder, free tier, supports forms
  - **GitHub Pages** — enable in repo settings, point to `docs/` branch
  - **Vercel** — connect repo, auto-deploys on push
- [ ] Point a custom domain (e.g. `bytessmith.com`) to the hosting platform
- [ ] Enable HTTPS (automatic on Netlify/Vercel/GitHub Pages)

### Future Enhancements
- [ ] Products page — dedicated showcase once AI products are ready to launch
- [ ] Case studies or client testimonials section
- [ ] Blog or insights section for SEO and thought leadership
- [ ] Analytics (e.g. Plausible or Google Analytics)
