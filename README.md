# TomKat Creative Website

Portfolio website for TomKat Creative, live at [tomkatcreative.com](https://tomkatcreative.com).

## Tech Stack

- [Eleventy](https://www.11ty.dev/) (v3) static site generator
- Nunjucks templates
- Deployed to GitHub Pages via GitHub Actions

## Development

```bash
npm install
npm run serve     # local dev server
npm run build     # build to _site/
```

## Deployment

Pushes to `master` automatically deploy via `.github/workflows/deploy.yml`. The workflow builds the site and deploys to GitHub Pages.

Custom domain is configured via `src/CNAME`.

## Project Structure

```
src/
  _data/          # Project data (animation, illustration, web)
  _includes/      # Nunjucks layouts and partials (base, nav, footer)
  css/            # Stylesheets
  gallery/        # Gallery pages (web, animation, illustration, project detail)
  img/            # Static images
  profiler/       # Profiler Party Game pages (privacy policy)
  contact.njk     # Contact page
  index.njk       # Home page
  CNAME           # Custom domain config
```

## Profiler Party Game

The [Profiler privacy policy](https://tomkatcreative.com/profiler/privacy-policy/) is hosted on this site at `src/profiler/privacy-policy.njk`. The Profiler game itself is a separate project; only its privacy policy lives in this repository.

## License

ISC
