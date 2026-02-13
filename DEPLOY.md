# Deployment Guide

## Quick Deploy to Netlify (Recommended - Free)

### Step 1: Push to GitHub

```bash
# Initialize git (if not already)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Create a new repo on GitHub, then:
git remote add origin https://github.com/YOUR-USERNAME/idea-space.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy on Netlify

1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub" and authorize Netlify
4. Select your `idea-space` repository
5. Build settings:
   - **Build command:** `npm run build`
   - **Publish directory:** `dist`
6. Click "Deploy site"

That's it! Your site will be live in ~1 minute at a URL like `random-name-12345.netlify.app`

### Step 3: Custom Domain (Optional)

1. In Netlify dashboard, go to "Domain settings"
2. Click "Add custom domain"
3. Follow instructions to point your domain to Netlify
4. Free SSL/HTTPS is automatic

## Future Updates

Every time you push to GitHub, Netlify automatically rebuilds your site.

### Adding a New Post

1. Create new `.md` file in `src/content/ideas/`
2. Add frontmatter and content
3. Commit and push:
   ```bash
   git add .
   git commit -m "New post: [title]"
   git push
   ```
4. Netlify rebuilds automatically (takes ~30 seconds)

## Alternative: Deploy to Vercel

Same process, just use [vercel.com](https://vercel.com) instead. Same build settings.

## Alternative: GitHub Pages

1. Install `@astrojs/github-pages` package
2. Update `astro.config.mjs` with site URL
3. Push to GitHub
4. Enable GitHub Pages in repo settings
5. Choose GitHub Actions as source

(Slightly more complex, Netlify is easier)

---

**Pro tip:** Once deployed, you can even add/edit posts directly on GitHub's website without touching code. Just browse to `src/content/ideas/`, click "Add file", paste your Markdown, and commit. Site rebuilds automatically.
