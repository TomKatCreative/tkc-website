# CLAUDE.md

## Project Overview

TomKat Creative portfolio site built with Eleventy v3, deployed to GitHub Pages at tomkatcreative.com.

## Commands

- `npm run serve` — local dev server with hot reload
- `npm run build` — build to `_site/`

## Architecture

- Static site generator: Eleventy 3 (ESM, `eleventy.config.js`)
- Templates: Nunjucks (`.njk`)
- Source: `src/` — Input directory
- Output: `_site/` — Build output (not committed)
- Data: `src/_data/projects.js` — all project entries, `src/_data/allProjects.js` — flat array
- Layouts: `src/_includes/base.njk` — main layout with SPA navigation and background transitions
- Deploy: GitHub Actions (`.github/workflows/deploy.yml`) on push to `master`
- Custom domain: `src/CNAME` → `tomkatcreative.com` (DNS via Squarespace)

## Key Conventions

- Passthrough copies: `src/img`, `src/css`, `src/CNAME`
- Background colors transition per page via `background` front matter key
- SPA-style client-side navigation (no full page reloads)
- Profiler Party Game privacy policy lives at `src/profiler/privacy-policy.njk` — the game itself is a separate project
