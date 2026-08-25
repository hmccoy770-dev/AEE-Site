# Apex Execution Engine — Site

Static landing page for AEE. This folder is meant to become a GitHub repo connected to Vercel for automatic deployments — every push to the main branch triggers a new live deployment, no manual upload needed.

## What's in here
- `index.html` — the full landing page (hero, classification, pricing, FAQ, footer)
- `logo.jpg` — the AEE logo, referenced by the page
- `vercel.json` — minimal Vercel config for a static site

## One-time setup (10–15 minutes)

### 1. Create the GitHub repo
1. Go to [github.com/new](https://github.com/new)
2. Name it something like `aee-site` (private or public, your call)
3. Don't initialize with a README — you already have one here
4. Create the repo

### 2. Push these files to it
From a terminal, inside this folder:
```bash
git init
git add .
git commit -m "Initial AEE site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/aee-site.git
git push -u origin main
```
Replace `YOUR-USERNAME` and the repo name with your actual GitHub details.

*(If you don't have git installed or aren't comfortable with the terminal, GitHub also lets you drag-and-drop these three files directly into a new repo through the web interface — look for "uploading an existing file" on the new repo page.)*

### 3. Connect the repo to Vercel
1. In the Vercel dashboard, go to your `hmccoy770-5234` team → **Add New → Project**
2. Choose **Import Git Repository** and select the `aee-site` repo you just created
3. Framework preset: choose **Other** (this is a plain static site, no build step needed)
4. Click **Deploy**

### 4. You're done
From this point on, every time you push a change to the `main` branch on GitHub, Vercel automatically builds and deploys it — live in under a minute, with zero manual steps. This is the "automatic" deployment pipeline without depending on the Vercel connector's permissions.

## Making future updates
- Edit `index.html` directly (or hand it back to Claude to edit), then:
  ```bash
  git add .
  git commit -m "Describe what changed"
  git push
  ```
- Vercel picks up the push and redeploys automatically.

## Notes
- Pricing, disclaimer language, and copy in `index.html` are current as of the last conversation — review before pointing real traffic at this.
- The legal/responsible-gambling disclaimer in the footer is draft language, not attorney-reviewed.
