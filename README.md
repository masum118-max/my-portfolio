# Portfolio: static site (no build step)

```
index.html                       the whole website (HTML + CSS + JS in one file)
cv/Tohidul-Islam-Khan-CV.pdf     placeholder: replace with your CV, keep the file name
images/profile.svg               placeholder: replace with your photo
favicon.svg
.nojekyll                        tells GitHub Pages to serve files as they are
```

## Edit

- Contact and profile links, and the publications list: the `CONFIG` and `PUBLICATIONS` blocks near the bottom of `index.html` (search for "EDIT THESE").
- Everything else is plain HTML. Search for `EDIT:` comments for places to add enrollment years, CGPA, thesis topic, GitHub links and project results.
- Photo: put `images/profile.jpg` in place and change `images/profile.svg` to `images/profile.jpg` in the hero section.
- After deploying, uncomment the `canonical` and `og:url` lines in `<head>` and set your real URL.

## Deploy on GitHub Pages

1. Create a new repository (e.g. `yourusername.github.io` for a root URL).
2. Upload all files in this folder (including `.nojekyll`) to the repository root.
3. Repository **Settings → Pages → Build and deployment**: Source "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
4. The site goes live at `https://yourusername.github.io/` within a minute or two.

## Deploy on Cloudflare Pages

1. Push the same repository to GitHub.
2. Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git**, and select the repository.
3. Framework preset: **None**. Build command: leave empty. Build output directory: `/`.
4. Save and deploy. Add a custom domain under **Custom domains**.

Alternative without Git: **Create → Pages → Upload assets**, and drag this folder in.

## Contact form

A static site has no server, so by default the form opens the visitor's email app with the message filled in. To receive messages directly, create a free form endpoint at formspree.io (or web3forms.com) and paste its URL into `formEndpoint` in the `CONFIG` block.
