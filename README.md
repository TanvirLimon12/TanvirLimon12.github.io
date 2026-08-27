# Tanvir Ahmed — personal academic website

Plain HTML and CSS. No build step, no dependencies.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site |
| `style.css` | Styling, light and dark mode |
| `Tanvir_Ahmed_CV.pdf` | CV linked from the sidebar and nav |
| `figures/` | 11 result figures pulled from the project repositories |
| `profile.jpg` | **Not included** — add a photo (see below) |

## Publish to GitHub Pages

The username is `TanvirLimon12`, so the site can live at `https://tanvirlimon12.github.io`.

1. Create a **new public repo named exactly** `TanvirLimon12.github.io`
2. From this folder:

```bash
git init
git add .
git commit -m "Add personal academic website"
git branch -M main
git remote add origin https://github.com/TanvirLimon12/TanvirLimon12.github.io.git
git push -u origin main
```

3. Repo → Settings → Pages → Source: `main`, folder `/ (root)`
4. Live in a minute or two at https://tanvirlimon12.github.io

## Add a profile photo

Put a square photo named `profile.jpg` in this folder, then in `index.html` replace:

```html
<div class="avatar-fallback">TA</div>
```

with:

```html
<img class="avatar" src="profile.jpg" alt="Tanvir Ahmed">
```

Until then the site shows a circular "TA" placeholder.

## Where the numbers come from

Every table and figure is reproduced from the committed `results/` and `figures/` directories
of the six project repositories — nothing is hand-entered from a paper draft. If a repo's
results change, re-pull the figure and update the matching table in `index.html`.

## Keeping it current

- **New paper accepted** — move its entry from the "Under Review" block to "Accepted" in `index.html`, and add a line to the News list.
- **New CV** — recompile `tanvir_cv.tex`, then copy it in:
  ```bash
  cp ../tanvir_cv.pdf Tanvir_Ahmed_CV.pdf
  ```
- **Google Scholar** — once the RAAICON paper indexes, add a link to the sidebar `<ul class="links">` list, matching the ORCID line.

## Local preview

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000
