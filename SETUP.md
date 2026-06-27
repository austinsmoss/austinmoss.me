# One-time setup: GitHub Pages + austinmoss.me

You only do this once. After that, updating the site is just "edit + publish."

## Step 1 — Make a free GitHub account
Go to https://github.com and sign up (free). Pick a username; it shows up in your
site's address during setup (e.g. `yourname.github.io`).

## Step 2 — Create a repository
1. Click the **+** (top right) → **New repository**.
2. Name it `austinmoss.me` (any name works).
3. Set it to **Public**. Don't add a README (we already have one).
4. Click **Create repository**.

## Step 3 — Upload the website files
Easiest option (no commands): on the new repo page, click **"uploading an existing
file"**, then drag in *everything* from this folder — `index.html`, `research.html`,
`teaching.html`, `cv.html`, the `css/` and `assets/` folders, `CNAME`, and `.nojekyll`.
Click **Commit changes**.

(Prefer the terminal? Just ask Claude Code to "push the site to GitHub" and it will
run the git commands for you.)

## Step 4 — Turn on GitHub Pages
1. In the repo, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)**. Click **Save**.
4. Wait ~1 minute. A green banner shows your live URL.

## Step 5 — Point austinmoss.me at GitHub
The `CNAME` file already tells GitHub your domain is `austinmoss.me`. Now tell your
domain registrar (wherever you bought austinmoss.me) to point at GitHub:

**Add these DNS records** (in your registrar's DNS settings):

| Type  | Host / Name | Value                                   |
|-------|-------------|-----------------------------------------|
| A     | @           | 185.199.108.153                         |
| A     | @           | 185.199.109.153                         |
| A     | @           | 185.199.110.153                         |
| A     | @           | 185.199.111.153                         |
| CNAME | www         | `YOURUSERNAME.github.io`                |

Replace `YOURUSERNAME` with your GitHub username. (Optional but recommended: also add
the four AAAA records from GitHub's docs for IPv6.)

Then back in **Settings → Pages → Custom domain**, enter `austinmoss.me`, Save, and
tick **Enforce HTTPS** once it becomes available (can take up to a few hours for DNS
to propagate).

That's it. Your site is live at https://austinmoss.me.

## Updating later
1. Edit content (ask Claude Code, or edit the `.html` files).
2. In GitHub, upload the changed file again **or** ask Claude Code to "publish my changes."
3. Live within a minute.
