# yulinliu2002.github.io

Personal site for Yulin (Jason) Liu — deployed at <https://yulinliu2002.github.io/>.

Plain HTML, hand-written CSS, vanilla JS. No build step, no frameworks.

---

## Stack

- **HTML** — `index.html` plus four project subpages in `work/`
- **CSS** — single stylesheet at `assets/css/main.css`
- **JS** — `assets/js/main.js` (mobile nav toggle, scroll reveal, nav shadow)
- **Fonts** — Fraunces / Inter / JetBrains Mono via Google Fonts

That's it. No npm, no Vite, no Tailwind, no CDN frameworks.

---

## Local development

Serve the repo root with any static file server. Python is fine:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000/>. Subpages live at `/work/<slug>.html`.

The site uses absolute paths starting with `/` (e.g. `/assets/css/main.css`), so it must be served from the repo root, not opened with `file://`.

---

## Deploying to GitHub Pages

The repo is the GitHub Pages user-site at `yulinliu2002.github.io`, so anything pushed to `main` is published.

One-time setup (already done if the site is live):

1. **Settings → Pages**, set **Source** to *Deploy from a branch*, branch **main**, folder `/` (root).
2. Add a `.nojekyll` file at the repo root so Pages doesn't try to run Jekyll.

That's it. Push to `main` and the site updates within a minute.

---

## File layout

```
index.html                     Home page
work/
  bioreactor.html              Cellxercise project page
  autonomous-vehicle.html      TranquiBot project page
  boomerang.html               Boomerang Aerodynamics project page
  xtreme-materials.html        Xtreme Materials project page
assets/
  css/main.css                 Single shared stylesheet
  js/main.js                   Mobile nav, reveal-on-scroll
  personal/                    Personal photos (band, portrait, family)
images/                        Project images, one folder per project
Jason_Liu_CV_2026.pdf          Linked from Contact section
```

---

## Editing content

- **Copy changes** — edit the relevant HTML directly. Sections are flagged in comments (`<!-- ============ HERO ============ -->`).
- **Photos** — drop new files into `assets/personal/` or `images/<project>/`. Reference them with absolute paths starting with `/`.
- **A new project page** — duplicate any file in `work/`, update title block, hero image, the four article sections (Context / Constraints / What I Built / Outcome), metric strip, gallery, and the "Next" link. Then add a tile to `index.html` inside `.work__grid`.

---

## Gotchas

- **Filenames are case-sensitive** on GitHub Pages (Linux servers). macOS APFS is case-insensitive locally, so a path that works on your laptop can 404 in production. Match file capitalisation exactly. The current site references `Autocar_new.JPG` (uppercase) on purpose.
- **Spaces in filenames** must be URL-encoded as `%20` in `src` attributes (e.g. `images/Boomerang/boomerang%20prototype.png`). Or rename the files to remove spaces — that's the more robust fix long-term.
- **Google Fonts** is loaded over the public network. Offline development still works; the page will fall back to the next font in the stack.
- **Reduced motion** — animations are disabled automatically when the user has `prefers-reduced-motion: reduce` set.

---

## Source of truth

`BRIEF.md` (in the repo) is the source of truth for site content — bio, project metrics, photo asset list. Edit BRIEF first, then update the HTML to match. Don't add facts or numbers to the site that aren't in BRIEF.
