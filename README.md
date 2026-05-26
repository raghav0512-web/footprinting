# Footprinting — Ready for GitHub & Vercel

This repository contains a static single-page site `index.html` (copied from `footprinting.html`) intended for deployment to Vercel or GitHub Pages.

Quick steps to push to GitHub:

1. Initialize git and commit

```bash
git init
git add .
git commit -m "chore: add footprinting site"
```

2. Create a remote repo and push

- Using GitHub website: create a new repo and follow the instructions to push
- OR with GitHub CLI:

```bash
gh repo create <owner>/<repo> --public --source=. --push
```

Deploy to Vercel (recommended):

Option A — Connect GitHub repo to Vercel (no CLI needed)
- Sign in at https://vercel.com and choose "Import Project" → connect your GitHub repo → Deploy. Vercel will serve `index.html` automatically.

Option B — Use Vercel CLI

```bash
npm i -g vercel
vercel login
vercel --prod
```

Notes
- Vercel serves static sites from the repository root; `index.html` must live at root (done).
- If you prefer automated deployments from GitHub, connect the repository in the Vercel dashboard.
- To deploy privately or via CI, set a `VERCEL_TOKEN` secret and use the Vercel CLI in your CI workflow.

If you want, I can:
- create a GitHub Actions workflow to auto-deploy using the Vercel token
- initialize the git repo and push (I will need your confirmation and GH repo URL or GH CLI auth)
