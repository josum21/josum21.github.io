# Zuchen Huang · 黄祖琛 — Personal Site

Single-page static personal CV + business-card site. Pure HTML / CSS / vanilla JS — no framework, no build step, no runtime dependencies.

## Run locally

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://127.0.0.1:8000
```

## Structure

```
index.html          # single page, all content
contact.html        # contact form (posts to Web3Forms → your email)
css/style.css       # design tokens, light/dark themes, responsive layout
js/main.js          # theme toggle, mobile nav, scroll reveal, scroll-spy
assets/             # favicon + images (placeholders until photos provided)
.dsh/skills/        # reusable DeepSeek Harness skill for this site
```

> The CV (`.docx` / `.pdf`) is intentionally **not** committed for privacy — it lives only locally and is git-ignored.

## Contact form

`contact.html` posts to [Web3Forms](https://web3forms.com) (free). To activate it, replace `YOUR_ACCESS_KEY` in `contact.html` with a real key from web3forms.com — the receiving email is configured there and stays hidden from the page.

## Edit content

Content lives directly in `index.html` under each `<section>`. See `.dsh/skills/static-personal-site/SKILL.md` for full conventions.

## Deploy (GitHub Pages, free)

1. Commit and push to the default branch of the `josum21.github.io` repo.
2. GitHub Pages publishes the `main` branch automatically for this user site.
3. Site live at `https://josum21.github.io/`.
