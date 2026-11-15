# byro-web

Source of https://byro.cloud, built with [Nikola](https://getnikola.com/).

- `master`: site sources (this branch) – edit here
- `gh-pages`: generated HTML, served by GitHub Pages – never edit by hand

## Setup

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## Edit & preview

Content lives in `pages/` (e.g. `pages/index.rst`), the theme in `themes/byro_theme/`.

```bash
nikola auto    # live preview at http://127.0.0.1:8000
```

## Deploy

Commit and push your changes to `master` first, then:

```bash
nikola github_deploy
```

This builds the site and force-pushes `output/` to `gh-pages`.
