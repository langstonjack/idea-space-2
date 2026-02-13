# Quick Start Guide

## What You Got

A complete website for sharing your ideas, built with:
- **Astro** (fast static site generator)
- **Tailwind CSS** (for styling)
- **Markdown** (simple content format)
- **3 example posts** (including your tomb track and dance challenge concepts)

## Next Steps

### 1. Download and Extract

Download the `idea-space` folder. This is your complete website.

### 2. Install Dependencies

Open Terminal/Command Prompt, navigate to the folder, and run:

```bash
cd idea-space
npm install
```

### 3. Run Locally

```bash
npm run dev
```

Open `http://localhost:4321` in your browser. You'll see your site running!

### 4. Try Adding a Post

1. Go to `src/content/ideas/`
2. Create a new file: `my-new-idea.md`
3. Add this at the top:

```markdown
---
title: "My New Idea"
description: "Testing out the posting system"
date: 2025-02-11
tags: ["test", "ideas"]
---

This is my content. I can write in **Markdown**.

## Headers work

- Lists work
- Everything just works
```

4. Save the file
5. The site auto-refreshes and shows your new post!

### 5. When You're Ready to Deploy

See `DEPLOY.md` for full instructions, but basically:

1. Push this folder to GitHub
2. Connect to Netlify (free)
3. Deploy
4. You're live!

## Customizing

### Change Colors

Edit `tailwind.config.mjs` and update the colors in the `extend` section.

### Change About Page

Edit `src/pages/about.astro` with your own bio/info.

### Add Social Links

Edit the footer in `src/layouts/BaseLayout.astro`.

## How Posting Works

Every `.md` file in `src/content/ideas/` becomes a post on your site.

**The filename becomes the URL:**
- `empty-tomb.md` → `yoursite.com/ideas/empty-tomb`
- `my-cool-idea.md` → `yoursite.com/ideas/my-cool-idea`

**Frontmatter controls metadata:**
```yaml
---
title: "Shows up as the headline"
description: "Shows up in the feed"
date: 2025-02-11
tags: ["clickable", "searchable"]
---
```

## Tips

- Keep it simple - just write in Markdown
- Tags help people find related content
- Embed Suno tracks, YouTube videos, whatever
- The site is fast because it's all static files
- You own all your content (it's just text files)

## Need Help?

Check the README.md for more details, or just ask me!

---

**You're good to go. Start sharing ideas.**
