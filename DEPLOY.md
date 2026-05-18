Deployment instructions
=======================

This repository contains a static site at the project root: `glowtogether.html`.

Options to deploy:

1) GitHub Pages (recommended)
   - Initialize git, commit files, push to a GitHub repository's `main` branch.
   - The included workflow `.github/workflows/deploy-pages.yml` will automatically deploy the repository root to GitHub Pages.

   Example:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

   After the push, go to the repository's Settings → Pages to verify the site URL.

2) Netlify
   - Drag-and-drop the repository root (or the built site) into Netlify Drop: https://app.netlify.com/drop
   - Or use the Netlify CLI: `netlify deploy --prod --dir=.` (requires `netlify` CLI and login)

3) Manual upload
   - Upload `glowtogether.html` (and any additional assets) to any static host or S3 bucket.

Notes:
- `.nojekyll` is included to prevent Jekyll processing on GitHub Pages.
- If you want the site to be served from the repository root, the workflow uploads the root as the artifact. If you'd prefer to publish a `docs/` folder or different path, update `deploy-pages.yml` accordingly.
