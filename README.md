# Jeff Personal Site

Built with [Astro](https://astro.build/) · Hosted on GitHub Pages.

## Quick Start

```bash
npm install
npm run dev       # localhost:4321
npm run build     # production build → dist/
```

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages → Source** → set to **GitHub Actions**
3. Push to `main` — the workflow auto-deploys

> **Before pushing:** Edit `astro.config.mjs` and replace `YOUR_GITHUB_USERNAME` with your actual GitHub username.

## Add Content

### New knowledge article
Create `src/pages/knowledge/my-article.md`:
```md
---
title: "Article title"
date: 2025-01-01
tags: [ckd, dialysis]
---

Your content here...
```

### New blog post
Create `src/pages/blog/my-post.md`:
```md
---
title: "Post title"
date: 2025-01-01
category: running
---

Your content here...
```

## Structure

```
src/
├── pages/
│   ├── index.astro         # Homepage
│   ├── knowledge/          # Clinical notes
│   └── blog/               # Personal writing
├── layouts/
│   └── BaseLayout.astro    # Shared nav + footer
public/
└── styles/global.css       # All styles
.github/workflows/
└── deploy.yml              # Auto-deploy
```
