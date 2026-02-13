# Idea Space

A clean, fast website for sharing concepts, half-baked ideas, and creative explorations. Built with Astro, styled with Tailwind.

## What This Is

This is a simple static site where you can drop ideas as they come. No complex CMS, no database, just Markdown files that become web pages.

## How It Works

### Adding a New Idea

1. Create a new `.md` file in `/src/content/ideas/`
2. Add frontmatter at the top with metadata
3. Write your content in Markdown
4. Deploy (site rebuilds automatically)

### Example Post Format

```markdown
---
title: "Your Idea Title"
description: "A short description that appears in the feed"
date: 2025-02-11
tags: ["tag1", "tag2", "tag3"]
---

Your content goes here in Markdown.

## You can use headers

And paragraphs, **bold text**, *italics*, [links](https://example.com), etc.

### Embedding Content

To embed a Suno track:
<iframe style="border-radius:12px" src="https://suno.com/embed/YOUR-TRACK-ID" width="100%" height="152" frameBorder="0" allowfullscreen></iframe>

To embed a YouTube video:
<iframe src="https://www.youtube.com/embed/VIDEO-ID" width="100%" height="400" frameborder="0" allowfullscreen></iframe>
```

## Project Structure

```
/
├── src/
│   ├── content/
│   │   ├── ideas/          # Your blog posts go here
│   │   └── config.ts       # Content collection schema
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro     # Homepage
│   │   ├── about.astro     # About page
│   │   ├── ideas/[slug].astro  # Individual post pages
│   │   └── tags/           # Tag pages
│   └── styles/
│       └── global.css
├── package.json
├── astro.config.mjs
└── tailwind.config.mjs
```

## Running Locally

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Deploying

This site is designed to deploy for free on:
- **Netlify** (recommended)
- **Vercel**
- **GitHub Pages**

### Netlify Setup (Easiest)

1. Push this repo to GitHub
2. Go to netlify.com
3. Click "Add new site" → "Import an existing project"
4. Connect your GitHub repo
5. Build command: `npm run build`
6. Publish directory: `dist`
7. Deploy!

Netlify will automatically rebuild whenever you push to GitHub.

## Customization

### Colors

Edit `/tailwind.config.mjs`:
```javascript
colors: {
  primary: '#0a0a0a',    // Main text color
  secondary: '#f5f5f5',  // Background
  accent: '#ff6b35',     // Highlight color
}
```

### Fonts

Edit `/tailwind.config.mjs`:
```javascript
fontFamily: {
  display: ['Your Display Font', 'serif'],
  body: ['Your Body Font', 'sans-serif'],
}
```

Don't forget to add the font import in `/src/styles/global.css`

### Adding Social Links

Edit the footer in `/src/layouts/BaseLayout.astro`

## Tips

- Keep post slugs simple (filename becomes the URL)
- Use tags consistently for better organization
- Embed content directly (Suno, YouTube, etc.)
- Write in plain Markdown for easy portability
- The site is fast because it's just static files
- Search engines can index everything

## The Philosophy

This site exists for sharing ideas transparently. Everything is vibed out with AI — the concepts are yours, the execution is collaborative. Own that. It makes the work more interesting, not less.

---

Questions? Just ask.
