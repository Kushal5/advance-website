# Advance Software — Website

Static marketing site + blog + case studies for **Advance Software** — software
engineering, data and AI systems plus Microsoft Dynamics 365 Business Central
development, for businesses in Fiji, the Pacific, Australia and beyond.

Built as a **Jekyll** site so GitHub Pages builds it automatically — publishing
a blog post or case study is just adding a markdown file and pushing. No build
tooling needed on your machine.

## Structure

```
index.html                  Homepage (v8 "circuit grid" design, picked from the review pack)
_config.yml                 Site config (title, plugins, collections)
_layouts/                   default / post / case-study page templates
_posts/                     Blog posts    → published at /blog/<slug>/
_case_studies/              Case studies  → published at /case-studies/<name>/
blog/index.html             Blog listing  → /blog/
case-studies/index.html     Case-study listing → /case-studies/
css/, assets/               Circuit-grid brand styling (no JS needed), logo + favicon
robots.txt, llms.txt        AI-crawler and answer-engine optimization (see below)
```

## Add a blog post

Create `_posts/YYYY-MM-DD-your-slug.md`:

```markdown
---
title: "Post title"
description: "One sentence for search results, social cards and AI answers."
date: 2026-07-10 09:00:00 +1200
tags: [Business Central, Automation]
---

Your markdown content here.
```

Push it. It appears at `/blog/your-slug/`, on the `/blog/` listing, in the RSS
feed, the sitemap and `llms.txt` — with Open Graph tags and JSON-LD structured
data generated automatically from the front matter.

## Add a case study

Copy `_case_studies/case-study-template.md`, rename it (filename = URL slug),
fill it in, and flip `published: false` to `published: true`. The template's
front matter (`industry`, `services`, `results`) drives the tags and the
results box at the top of the page.

**Copy guardrails** (keep these): BC *developer*, never a reselling "partner";
no public pricing; verifiable, sourced claims only; no AI-delivery promises;
lead with global standards, not Suva; no founder name on the site for now;
automation copy sells *building* the automation, not doing the back-office work.

## Deploy to GitHub Pages (one-time, ~5 minutes)

> Do this from your **personal** GitHub account.

1. Create a new **public** repo on github.com (e.g. `advance-website`).
2. From this folder (use a personal identity for a public repo):
   ```
   git init -b main
   git config user.name  "Your Name"
   git config user.email "kush.pillay7@gmail.com"
   git add .
   git commit -m "Advance Software site"
   git remote add origin https://github.com/<you>/advance-website.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root)**.
4. Live in ~a minute at `https://<you>.github.io/advance-website/`.

No URL configuration needed — GitHub fills in `site.url`/`baseurl` from the
repo automatically. If you later add a custom domain, set `url:` (and empty
`baseurl:`) in `_config.yml` and add a `CNAME` file.

## Preview locally (optional)

The homepage works by just opening `index.html`, but blog/case-study pages
need Jekyll. One-time setup: install Ruby (rubyinstaller.org, with DevKit),
then:

```
gem install jekyll jekyll-seo-tag jekyll-sitemap jekyll-feed
jekyll serve    # → http://localhost:4000
```

## AI search optimization (what's built in)

- **JSON-LD structured data** — `ProfessionalService` schema on the homepage;
  `BlogPosting` on every post (via jekyll-seo-tag); `FAQPage` where a post has
  an FAQ section.
- **`llms.txt`** — a machine-readable site summary for AI answer engines,
  auto-updated with every post/case study.
- **`robots.txt`** — explicitly welcomes AI crawlers (GPTBot, ClaudeBot,
  PerplexityBot, Google-Extended, etc.) and points at the sitemap.
- **`sitemap.xml` + RSS `feed.xml`** — generated on every build.
- **Semantic HTML** — `<article>`, `<time>`, one `<h1>` per page, descriptive
  meta descriptions from front matter.
- Descriptions and sourced claims in posts are written to be quotable by
  answer engines — keep doing that in new content.

## Still pending

- **Booking link** — CTAs use `mailto:`; swap for Calendly when ready
  (search `mailto:` in `index.html` and `_layouts/`).
