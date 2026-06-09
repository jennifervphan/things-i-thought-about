# things i thought about

A personal blog built with [Astro](https://astro.build) and [Tailwind CSS](https://tailwindcss.com). Posts are written in Markdown and deployed automatically to [Netlify](https://netlify.com).

## Local development

```bash
npm install
npm run dev
```

Opens at `http://localhost:4321`.

## Writing a post

Create a new `.md` file in `src/content/posts/`:

```md
---
title: "Your title"
description: "A short summary shown on the home page"
pubDate: "2026-06-09"
tags: ["optional", "tags"]
---

Your content here...
```

The filename becomes the URL slug — `my-post.md` → `/posts/my-post`.

Posts are sorted by `pubDate`, newest first.

## Deploying

Push to GitHub, then connect the repo to Netlify:

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import an existing project**
2. Select your GitHub repo
3. Netlify auto-detects the `netlify.toml` — no configuration needed
4. Click **Deploy site**

After that, every push to `main` triggers an automatic redeploy.

## Project structure

```
src/
├── content/posts/    ← write posts here
├── layouts/          ← BaseLayout, PostLayout
├── components/       ← PostCard
└── pages/            ← index, about, posts/[slug]
public/               ← static assets (favicon, images)
netlify.toml          ← build config
```
