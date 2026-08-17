# CMSSW Knowledge Base

A learning-oriented, source-linked guide to CMSSW. Markdown in `docs/` is the
source of truth; MkDocs Material turns it into a searchable static website.

## Local preview

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000/cmssw-knowledge/>. MkDocs rebuilds the site while
source files are edited.

## Static HTML build

```bash
source .venv/bin/activate
mkdocs build --strict
```

The complete static website is written to `site/`. Copy the entire directory's
contents—including `assets/`, `search/`, and JavaScript files—to another web
server when needed.

## GitHub Pages

Pushes to `main` run `.github/workflows/pages.yml`. In the GitHub repository,
select **Settings → Pages → Build and deployment → GitHub Actions** once. The
published project site is:

<https://de-cristo.github.io/cmssw-knowledge/>
