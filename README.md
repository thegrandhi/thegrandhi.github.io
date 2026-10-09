# thegrandhi.github.io

My personal site. Plain HTML and CSS with no build step.

- `index.html`: all the content
- `styles.css`: colors, type and layout (tokens at the top, dark mode right below)
- `assets/`: project screenshots as WebP
- `favicon.svg`: the tab icon

## Preview locally

```bash
python3 -m http.server 4400
```

Then open http://localhost:4400.

## Publish on GitHub Pages

A repository named `thegrandhi.github.io` is served at https://thegrandhi.github.io/. Broadsheet keeps working at `/broadsheet/`.

```bash
git init -b main
git add .
git commit -m "First version of the site"
gh repo create thegrandhi.github.io --public --source . --push
```

GitHub publishes the `main` branch automatically. If it doesn't, turn it on under **Settings → Pages → Deploy from a branch → main / (root)**.

## Adding a project screenshot

Save a PNG, convert it, and reference it with its real `width` and `height` so the page doesn't shift while it loads:

```bash
cwebp -q 82 -resize 1800 0 screenshot.png -o assets/project.webp
```
