# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Stack

- **Framework**: [Astro](https://astro.build) v5 (minimal template)
- **Hosting**: Vercel (static output)
- **Language**: TypeScript (via tsconfig.json)

## Commands

```bash
npm run dev       # start local dev server at localhost:4321
npm run build     # build for production (output: dist/)
npm run preview   # preview production build locally
```

## Project Structure

```
src/
  pages/         # file-based routing — each .astro file is a route
  layouts/       # (add shared layouts here)
  components/    # (add reusable components here)
public/          # static assets served at root (favicon, images, etc.)
```

## Architecture Notes

- Astro pages use a frontmatter fence (`---`) for server-side logic; everything below is the template.
- Zero client-side JS by default. Add interactivity with `client:*` directives only when needed.
- New pages are created by adding `.astro` (or `.md`) files under `src/pages/`.
- Shared HTML structure (head, nav, footer) should live in `src/layouts/` and be imported into pages.
- Vercel auto-detects Astro — no extra config needed for deployment.
