# Publishing this portfolio with Git and GitHub Pages

This folder is a complete static site (no build step). All paths are relative, so it works at
`https://altasdid.github.io/` and at `https://altasdid.github.io/altasdid/`.

## Option A (recommended): root URL https://altasdid.github.io/
1. On GitHub create a new **public** repository named exactly `altasdid.github.io` (empty, no README).
2. In a terminal, from inside this folder:
   ```
   git init -b main
   git add .
   git commit -m "Add portfolio website"
   git remote add origin https://github.com/altasdid/altasdid.github.io.git
   git push -u origin main
   ```
3. On GitHub: repository **Settings > Pages > Build and deployment > Source: Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. Wait 1 to 2 minutes. The site is live at https://altasdid.github.io/

## Option B: use your existing repo https://github.com/altasdid/altasdid
That repository is your profile README repo. Adding the site there works, but do not overwrite its `README.md`.
```
git clone https://github.com/altasdid/altasdid.git
# copy everything from this folder into it (index.html, css, js, img, video, .nojekyll), keep its README.md
cd altasdid
git add .
git commit -m "Add portfolio website"
git push
```
Then **Settings > Pages > Deploy from a branch > main / root**. The site will be at https://altasdid.github.io/altasdid/

## Updating later
Edit the files, then `git add . && git commit -m "Update" && git push`. Pages redeploys automatically.

## Folder map
- `index.html` all content (edit text here)
- `css/style.css` colors are variables at the top (`--red`, `--ink`, `--bone`)
- `js/main.js` tabs, project filter, copy-email, photo viewer
- `img/` photos and certificates, `video/` line-follower clip
