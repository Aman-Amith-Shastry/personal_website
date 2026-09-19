# Personal website

Static site — plain HTML and CSS, no build step, no external requests. Deployed on GitHub Pages.

```
index.html    all content
styles.css    all styling
assets/       figures referenced by the page
.nojekyll     serve files as-is, skip Jekyll processing
```

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploying to GitHub Pages

For a site at `https://<username>.github.io`, the repository must be named
`<username>.github.io`. Any other repository name publishes to
`https://<username>.github.io/<repo>/`.

```bash
git init -b main
git add .
git commit -m "Personal website"
git remote add origin git@github.com:Aman-Amith-Shastry/Aman-Amith-Shastry.github.io.git
git push -u origin main
```

Then in the repository: **Settings → Pages → Build and deployment → Source: Deploy from a
branch**, branch `main`, folder `/ (root)`. The first build takes a minute or two.

## Editing

Every section is a `<section>` in `index.html` with a comment marking it. Projects and roles
are `<article class="entry">` blocks — copy one to add another. Order inside the Projects
section is most-recent-first by hand; there is no sorting logic.

Colors, fonts, and the text measure are the custom properties in the `:root` block at the top
of `styles.css`.
