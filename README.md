# personal-website

Jeffrey Li's personal website.

A single-page personal site: name/tagline, about, projects, and contact.
Built as plain static HTML/CSS/JS — no build step, no framework, no
dependencies beyond a local dev server — so it's cheap to host and easy to
iterate on.

## Stack

- Plain HTML, CSS, and vanilla JS (`index.html`, `styles.css`, `script.js`).
- No build tooling. Any static file host works as-is.

## Running locally

Any static file server works. Two easy options:

```sh
# Option A: no install needed if you have Python 3
python3 -m http.server 5173

# Option B: via npm (uses the `serve` package, no global install)
npm start
```

Then open http://localhost:5173 in a browser.

## Project structure

```
index.html    # page content and structure
styles.css    # all styling (light/dark aware, responsive)
script.js     # mobile nav toggle + footer year
```

## Editing content

All page copy lives directly in `index.html` — update the hero tagline,
About paragraph, project cards, and contact links there. Styling is
token-based at the top of `styles.css` (colors, spacing, max width) if you
want to retheme without touching layout rules.

## Deploying

Not yet wired up. Because this is a static site with no build step, it can
be deployed as-is to any static host, for example:

- **GitHub Pages**: point Pages at the repo root (or add a simple Actions
  workflow) — no build step required.
- **Netlify / Vercel**: import the repo, leave the build command empty, and
  set the publish/output directory to the repo root.
