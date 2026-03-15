# Bytes Smith — Official Website

Static marketing website for [Bytes Smith](https://bytessmith.com), a Singapore-based AI company offering AI products, custom AI solutions, and AI services & consultancy.

## Pages

| File | Page |
|------|------|
| `docs/index.html` | Homepage — hero, services overview, trust strip, CTA |
| `docs/services.html` | Services detail — three pillars with full descriptions |
| `docs/about.html` | About — company story, values, Singapore context |
| `docs/contact.html` | Contact — enquiry form with service selector |

## Stack

Plain HTML5 + CSS3 + vanilla JS. No framework, no build step, no dependencies.

- Fonts: Inter via Google Fonts
- Styles: `docs/css/style.css`
- Scripts: `docs/js/main.js`

## Deployment

Deploy the `docs/` folder to any static host (Netlify, Vercel, GitHub Pages).

For the contact form, add a form backend before going live:
- **Formspree** — set `action="https://formspree.io/f/{id}"` on the form
- **Netlify Forms** — add `data-netlify="true"` to the form element

## Docs

- [`documentation/project_overview.md`](documentation/project_overview.md) — goals, design direction, site structure
- [`documentation/techs/technical-specs.md`](documentation/techs/technical-specs.md) — stack, CSS tokens, file structure
- [`project/project-progress.md`](project/project-progress.md) — what's done and next steps
