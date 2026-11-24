# Security blog (Jekyll + Chirpy on GitHub Pages)

Built from the official [chirpy-starter](https://github.com/cotes2020/chirpy-starter) (Chirpy v7.6). The theme comes in as a gem, so this repo only holds your config and posts.

## Before the first publish

1. Optional: add your LinkedIn URL in `_config.yml` (`social.links`) and uncomment the LinkedIn block in `_data/contact.yml`.
2. Optional: read `_tabs/about.md` and adjust the wording.

## Publish

1. On GitHub, create a new public repository named `s7rid3r.github.io` (empty: no README, license or .gitignore).
2. From this folder:

   ```bash
   git init -b main
   git add .
   git commit -m "Initial blog"
   git remote add origin https://github.com/s7rid3r/s7rid3r.github.io.git
   git push -u origin main
   ```

3. In the repo, open **Settings > Pages** and set **Source** to **GitHub Actions**.
4. Open the **Actions** tab and wait for "Build and Deploy" to go green (re-run it if it ran before step 3).
5. The site is live at https://s7rid3r.github.io

If you use a different repo name, the site lives at `https://s7rid3r.github.io/<repo>` and you need to set `baseurl: "/<repo>"` in `_config.yml`.

## Writing a new post

Add `_posts/YYYY-MM-DD-short-title.md`:

```yaml
---
title: "Post title"
date: 2026-12-01 20:00:00 -0600
categories: [Write-ups, AI Red Teaming]
tags: [prompt-injection, portswigger]
description: One-sentence summary shown in previews.
---
```

Push to `main` and the site rebuilds. A post dated in the future won't show until that time passes.

## Preview locally (optional)

```bash
bundle install
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000.
