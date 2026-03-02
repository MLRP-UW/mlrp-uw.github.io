# MLRP Website — Agent Context

## Project Overview

Website for the Machine Learning Reading Program (MLRP) at the University of Washington.
Built with Astro + Tailwind CSS v4, deployed to GitHub Pages via GitHub Actions.

## Tech Stack

- **Framework**: Astro v5 (static site generator)
- **Styling**: Tailwind CSS v4 (utility-first, configured via `@theme` in `src/styles/global.css`)
- **Font**: Geist Sans (via `@fontsource/geist-sans`)
- **Deploy**: GitHub Pages via `.github/workflows/deploy.yml`

## Project Structure

```
src/
  components/   → Reusable Astro components (Navbar, Footer, etc.)
  data/         → JSON data files for site content (edit these to update content)
  layouts/      → Page layouts (Layout.astro is the base)
  pages/        → File-based routing (each .astro file = a page)
  styles/       → Global CSS with Tailwind and design tokens
public/         → Static assets (images, favicon)
```

## Design System

All design tokens are defined in `src/styles/global.css` under `@theme`:

- Background: `cream` (#FAF9F5), `cream-dark` (#F0EFEB)
- Text: `text` (#1A1A1A), `text-muted` (#6B6B6B), `text-light` (#999999)
- Accent: `accent` (#4A7C6F)
- Dividers: `divider` (#E5E4E0)
- Font: Geist Sans

Use these as Tailwind classes: `bg-cream`, `text-text-muted`, `border-divider`, etc.

## Content Management

- **Site-wide content** (name, social links, forms, navigation): Edit `src/data/site.json`
- **Page content**: Edit the corresponding `.astro` file in `src/pages/`
- **Google Form URLs**: Update in `src/data/site.json` under `forms.mentee` and `forms.mentor`

## Commands

- `npm run dev` — Start dev server
- `npm run build` — Build for production
- `npm run preview` — Preview production build locally

## Key Conventions

- Pages use the shared `Layout.astro` which includes Navbar and Footer
- Content sections use `max-w-3xl mx-auto px-6` for consistent narrow centered layout
- Sections are separated by `<hr class="mx-auto max-w-3xl border-divider" />`
- Navigation links are driven by the `navigation` array in `site.json`
- Pages on hold (Calendar, FAQ, Team) exist as stubs but are not in the nav
