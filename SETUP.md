# Eco‑Audit Pro — Rule Catalog Site

This is a ready‑to‑serve **MkDocs** site that organizes the Eco‑Audit Pro rule pages by technology.

## Quick start
```bash
python -m venv .venv && source .venv/bin/activate
pip install mkdocs mkdocs-material
mkdocs serve
```

Open `http://127.0.0.1:8000`.

## Deploy
- **GitHub Pages:** add a workflow that runs `mkdocs gh-deploy --force`
- **Static hosting:** use `mkdocs build` and publish the `site/` folder.



## Publish to GitHub Pages (GitHub Actions)
1. Push this folder to the root of your repo (keep `mkdocs.yml` and `docs/` at the repo root).
2. Commit `.github/workflows/deploy-mkdocs.yml`.
3. In your repository settings → **Pages**, set **Build and deployment** to **GitHub Actions**.
4. Push to `main` (or `master`). The workflow will build with MkDocs and deploy the contents of `site/`.
5. Your site will be available at the URL shown in the workflow output (usually `https://<org_or_user>.github.io/<repo>`).

### Custom domain (optional)
- Add a `CNAME` file under `docs/` containing your domain (e.g., `docs/CNAME` with `docs.example.org`).
- Configure a DNS `CNAME` to `<org_or_user>.github.io`.
