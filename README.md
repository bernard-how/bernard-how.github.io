# Portfolio Site

A plain static site (no build step, no framework) ready for GitHub Pages.

## Structure

```
site/
├── index.html          # Home page with the trail-map nav
├── about.html
├── projects.html
├── contact.html
├── blog/
│   ├── index.html       # Post list
│   └── first-post.html  # Example post
└── assets/
    ├── css/style.css    # One shared stylesheet for every page
    └── js/main.js       # Highlights the current page in the nav
```


## Preview locally

Opening `index.html` directly in a browser works for most of the site. If you
want to test exactly as GitHub Pages will serve it, run a local server from
this folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a repository named `yourusername.github.io` (this makes it your
   root personal site — use any other repo name if you want it at
   `yourusername.github.io/reponame` instead).
2. Push the contents of this `site/` folder to the repository root:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages → Source**, select the `main`
   branch and `/ (root)` folder, then save.
4. Your site will be live at `https://yourusername.github.io` within a
   minute or two.

No build tooling is required. it's just static HTML/CSS/JS, so it deploys as-is.
