# byro-web

Source of https://byro.cloud, built with [Nikola](https://getnikola.com/).

byro.cloud only redirects to the new website https://byro.info/.

- `master`: site sources (this branch) – edit here
- `gh-pages`: generated HTML, served by GitHub Pages – never edit by hand

## Setup

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## Edit & preview

The redirect page is `files/index.html`, the redirect for `/de/` is `REDIRECTIONS` in `conf.py`.

```bash
nikola auto    # live preview at http://127.0.0.1:8000
```

## Deploy

Commit and push your changes to `master` first, then:

```bash
nikola github_deploy
```

This builds the site and pushes `output/` to `gh-pages`.
