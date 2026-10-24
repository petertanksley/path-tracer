# Path Tracer

Source for the Path Tracer website: explainer videos on the methods of biosocial science, presented as a game of
realms (topics) and sectors (episodes). Videos are hosted on YouTube and embedded here.

Most pages are **generated**. `index.qmd`, `realms/` and `sectors/` are written by `tools/publish.R` in the (separate,
non-git) production folder from its `episodes.yml` registry. Edit the registry, not the pages. Hand-written:
`_quarto.yml`, `about.qmd`, `theme/`, `assets/favicon.svg`.

```bash
# from the production folder
Rscript tools/publish.R            # regenerate pages into ~/Documents/GitHub/path-tracer
# from this folder
quarto preview                     # look before committing
```

Pushing to `main` renders the site with Quarto and deploys it to GitHub Pages (`.github/workflows/publish.yml`). The
build needs only Quarto, not R.
