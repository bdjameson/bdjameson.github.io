# Personal site starter (Quarto + GitHub Pages)

This is a ready-to-go scaffold for a free personal/academic website, styled after
sites like https://nbaetge.github.io/. Total cost: **$0/year** (or ~$12/year if
you add a custom domain).

## What's included
- `_quarto.yml` — site config (navbar, theme)
- `index.qmd` — About/home page
- `research.qmd` — Research overview
- `publications.qmd` — Publications list
- `cv.qmd` — CV page
- `styles.css` — light custom styling
- `.github/workflows/publish.yml` — auto-builds and deploys the site on every push

## One-time setup

1. **Install Quarto** (free): https://quarto.org/docs/get-started/
   - Mac: `brew install --cask quarto`
   - Or download the installer for your OS

2. **Create the GitHub repo.** It MUST be named exactly:
   `yourusername.github.io`
   (replace `yourusername` with your actual GitHub username — this exact
   naming is what makes GitHub Pages auto-host it for free)

3. **Edit the placeholder content:**
   - Swap in your real name, links, email, LinkedIn/GitHub handles in `_quarto.yml`
   - Fill in `cv.qmd`, `publications.qmd`, `research.qmd` with your details
   - Optionally drop a photo into an `images/` folder and reference it in `index.qmd`

4. **Push to GitHub:**
   ```bash
   cd personal-site
   git init
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git add .
   git commit -m "Initial site"
   git branch -M main
   git push -u origin main
   ```

5. **Enable GitHub Pages:**
   - Go to your repo → Settings → Pages
   - Under "Build and deployment", set Source to **GitHub Actions**
     (the included workflow handles the rest automatically)

6. **Wait ~2 minutes**, then visit `https://yourusername.github.io` — it's live.

## Making updates later
Just edit any `.qmd` file and push:
```bash
git add .
git commit -m "Update CV"
git push
```
The GitHub Action rebuilds and redeploys automatically — no manual rendering needed.

## Optional: custom domain
If you want `carysjohnson.com` instead of `.github.io`:
1. Buy the domain (~$10-15/year) from a registrar like Namecheap or Cloudflare
2. Add a `CNAME` file to the repo root containing just your domain name
3. Point the domain's DNS A records at GitHub's IPs (instructions:
   https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## Local preview before publishing
```bash
quarto preview
```
This opens a live-reloading local preview in your browser so you can check
changes before pushing.
