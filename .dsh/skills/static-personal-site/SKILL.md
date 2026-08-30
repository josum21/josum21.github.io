---
name: static-personal-site
description: Build, edit, and deploy the single-page static personal CV/business-card website for Dr. Zuchen Huang (pure HTML/CSS/JS, no framework, no build step), including content updates and free GitHub Pages deployment.
whenToUse: When creating, editing, restyling, or deploying this personal site — adding/removing sections, updating CV content, changing design tokens, or publishing to GitHub Pages.
---

# Static Personal Site

Single-page static CV + business-card site. No framework, no build step, no runtime dependencies — it must run by opening `index.html` directly or serving the folder with any static file server.

## Stack & Layout

- `index.html` — single page; semantic `<section>` blocks with anchor navigation.
- `contact.html` — contact form page; posts to a form backend (Web3Forms) that forwards to email.
- `css/style.css` — design tokens via CSS custom properties; light/dark themes; responsive layout.
- `js/main.js` — theme toggle (localStorage + prefers-color-scheme), mobile nav, scroll reveal, scroll-spy.
- `assets/` — favicon and images. Avatar and project images are placeholders until real photos are supplied.

## Content Sources & Privacy

- The CV (`CV_ZuchenHuang.docx` / `.pdf`) is the authoritative content source but is **local-only and git-ignored** — never commit or publish it.
- Identity: Dr. Zuchen Huang (黄祖琛). Primary language is English; key information is also shown in Chinese.
- The email address must not appear in page markup; contact goes through the `contact.html` form.

## Editing Content

1. Edit the matching `<section>` in `index.html`. Timeline entries are `<article class="entry">` blocks; bullet details are `<li>` items.
2. Keep the "no-build" contract — never introduce a bundler, framework, or runtime dependency.
3. Use `<sup>`/`<sub>` HTML tags for particle-physics notation (e.g. `D<sup>*±</sup> → e<sup>±</sup>ν<sub>e</sub>`).
4. Profile links (ORCID, INSPIRE-HEP, GitHub, GitLab, LinkedIn) are icon links in the hero.

## Contact Form (Web3Forms)

- Form lives in `contact.html`; endpoint `https://api.web3forms.com/submit`, hidden `access_key` (replace the `YOUR_ACCESS_KEY` placeholder), honeypot `botcheck`, and `redirect` back to the page with `?sent=1`.
- The receiving email is configured on web3forms.com and is never exposed in the site.

## Deploy (GitHub Pages, free)

1. Ensure git is initialized and pushed to the `josum21.github.io` repo (`git@github.com:josum21/josum21.github.io.git`).
2. Commit and push to `main`; GitHub Pages publishes the `main` branch automatically for this user site.
3. Site is live at `https://josum21.github.io/`.

## Conventions

- Semantic, accessible HTML (alt text, aria-labels, keyboard-focusable controls).
- Responsive first (mobile → desktop).
- Minimal single accent color; refine visuals later without changing markup.
