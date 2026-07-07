# Raymond R. Silot — Portfolio

A single-page, slideshow-style portfolio site. Dark, terminal/ledger-inspired look, built with plain HTML/CSS/JS — no build step, no dependencies to install.

**Live demo:** once deployed (see below), your site will be at
`https://<your-username>.github.io/<repo-name>/`

## Navigation

- **Arrow keys** (← / →) to move between slides
- **On-screen arrows** at the bottom
- **Swipe** left/right on mobile
- **Dots** on the right edge (desktop) jump to any slide

## Structure

```
.
├── index.html    # everything lives here — markup, styles, and script
├── README.md
└── assets/
    └── profile.png   # hero photo
```

## Running locally

No build tools needed. Either:

- Double-click `index.html` to open it in a browser, or
- Serve it locally for a more accurate preview:
  ```bash
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000`

## Deploying to GitHub Pages

1. Push this folder to a new GitHub repository.
2. In the repo, go to **Settings → Pages**.
3. Under **Source**, select the `main` branch and `/ (root)` folder.
4. Save. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Editing content

Everything is in `index.html`:

- **Hero / name / role** — the first `<section class="slide" data-index="0">`
- **Experience entries** — look for `.entry` blocks inside `data-index="2"`, one per job
- **Skills** — the `.tag` list inside `data-index="3"`
- **Contact** — `data-index="5"`, update the `mailto:` link

Colors, fonts, and spacing are set as CSS variables at the top of the `<style>` block (`:root`), so you can retheme the whole site by changing a handful of values.

## Notes

Personal details like home address, birth date, and other private information were intentionally left off this public-facing version — only name and email are shown. Add a phone number or LinkedIn link in the contact slide if you'd like recruiters to have another way to reach you.
