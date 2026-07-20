# MusicCast — Website

Official marketing site for MusicCast, the white-label distribution platform for music distributors. Built with [Astro](https://astro.build) and deployed as a Cloudflare Worker.

Brand: black background, white text, magenta (`#ff00ff`) accent.

## Project structure

- `src/pages/index.astro` — landing page (hero, features, how it works, integrations, CTA)
- `src/pages/about.astro` — about page
- `src/components/` — `Header`, `Footer`, `BaseHead` (SEO/meta tags)
- `src/styles/global.css` — brand theme (CSS custom properties) and shared building blocks (`.btn`, `.section`, `.card`, etc.)
- `src/content/blog/` — blog content collection (scaffolded, not currently linked from navigation)
- `public/` — static assets (favicon, OG image, fonts)

## Commands

All commands run from the root of the project:

| Command           | Action                                      |
| :----------------- | :------------------------------------------ |
| `npm install`       | Install dependencies                        |
| `npm run dev`       | Start local dev server at `localhost:4321`  |
| `npm run build`     | Build the production site to `./dist/`      |
| `npm run preview`   | Build and preview locally before deploying  |
| `npm run deploy`    | Deploy to Cloudflare Workers                |
| `npm run check`     | Build + typecheck + dry-run deploy          |

## Deploying

```bash
npm run build
npm run deploy
```

The Worker name is `mc-website` (see `wrangler.json`). The configured site URL is `https://musicca.st` (`astro.config.mjs`) — update this if the marketing site is served from a different domain.
