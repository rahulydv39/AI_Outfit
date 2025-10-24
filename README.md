# AI Fashion Outfit

Static HTML demo app for an AI-powered outfit styling UI. This repository contains a simple front-end that allows a user to upload a model photo, an optional clothing photo, apply style templates, and call a Generative Language API to produce an edited image or a critique. The example includes placeholders for API keys which must be provided in `1.html` before using those features.

Contents:

- `1.html` — The main static HTML file (UI + JS). You may want to rename this to `index.html` for hosting.
- `ai-fashion-outfit/` — Existing subfolder containing another copy of the site (index, assets, css, js).
- `assets/`, `css/`, `js/` — Static assets and scripts (already present inside `ai-fashion-outfit`).

Quick local preview

Open `1.html` or `ai-fashion-outfit/index.html` in a browser (double-click or use a static server):

macOS (Python 3):

```bash
python3 -m http.server 8000
# then open http://localhost:8000/1.html
```

Or if you rename `1.html` to `index.html` and want to preview the folder:

```bash
python3 -m http.server 8000
# open http://localhost:8000/
```

Important notes

- The JavaScript in `1.html` calls Google Generative Language endpoints and expects an API key to be inserted in the `apiKey` constants inside the file. Do NOT commit secrets to the repo. Use environment-based injection or a private config for production.
- The project is static; you can host on GitHub Pages once pushed to a repository.

How to create a GitHub repo and push (recommended commands)

1) Using GitHub web: create a new repo named `ai-fashion-outfit` (public or private). Copy the remote URL, then run locally:

```bash
git remote add origin <REMOTE_URL>
git push -u origin main
```

2) Using GitHub CLI (if installed and authenticated):

```bash
gh repo create your-username/ai-fashion-outfit --public --source=. --remote=origin --push
```

Security: never paste API keys into public commits. Use a `.env` or build-time injection for production.

If you want, provide the repo name and permission (or a PAT) and I can attempt to create the remote for you automatically.
