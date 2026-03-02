# MLRP — Machine Learning Reading Program

Website for the [Machine Learning Reading Program](https://mlrp-uw.github.io) at the University of Washington.

## Development

```bash
npm install        # Install dependencies
npm run dev        # Start dev server at localhost:4321
npm run build      # Build for production
npm run preview    # Preview production build
```

## Updating Content

Most content can be updated by editing `src/data/site.json` — this controls the site name, navigation links, social links, Google Form URLs, and footer text.

Page-specific content is in the `.astro` files under `src/pages/`.

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to `main` via the GitHub Actions workflow in `.github/workflows/deploy.yml`.

## Tech Stack

- [Astro](https://astro.build) — Static site generator
- [Tailwind CSS](https://tailwindcss.com) — Utility-first CSS
- [Geist Sans](https://vercel.com/font) — Typography
