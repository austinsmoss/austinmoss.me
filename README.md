# austinmoss.me

My personal academic website. Plain HTML/CSS — no build step, nothing to install.

## How to update it (the easy way)

Open this folder in **Claude Code** and just say what you want, e.g.:

- "Add this paper to my research page: [title, coauthors, journal, link]"
- "Update my bio on the homepage."
- "Add a new course to the teaching page."
- "Change the accent color to navy."

Claude edits the file, you see it in the preview, and then publish (below).

## How to update it by hand (if you ever want to)

Everything is plain text:

| To change…            | Edit this file        |
|-----------------------|-----------------------|
| Bio, photo, contact   | `index.html`          |
| Papers                | `research.html`       |
| Courses               | `teaching.html`       |
| CV link               | `cv.html`             |
| Colors, fonts, layout | `css/style.css` (top) |
| Your photo / CV PDF   | `assets/`             |

To preview locally, just double-click `index.html` to open it in a browser.

## How to publish changes

This site is hosted on **GitHub Pages**. After editing, publish with:

```bash
git add -A
git commit -m "Update site"
git push
```

Changes go live at https://austinmoss.me within a minute or two.

## First-time setup notes

- Custom domain is configured via the `CNAME` file (`austinmoss.me`).
- `.nojekyll` tells GitHub Pages to serve the files as-is (no Jekyll build).
- See `SETUP.md` for the one-time GitHub + DNS steps.
