# shulian.dev

Personal portfolio of Julián Antonucci — senior backend engineer (Node.js, distributed systems, AWS).

Built with [Astro](https://astro.build), deployed on [Vercel](https://vercel.com).

## Develop

```sh
npm install
npm run dev      # http://localhost:4321
npm run build    # static output → dist/
npm run preview  # serve the built site locally
```

## Structure

| Path | What |
| --- | --- |
| `src/pages/index.astro` | the entire single-page site + styles |
| `src/layouts/Base.astro` | `<head>`, fonts, meta, theme bootstrap |
| `public/favicon.svg` | favicon |

## Editing content

Everything is in `src/pages/index.astro`:

- **Case studies** — `<article class="case">`. Case 1 (ink-cover) is real; cases 2 & 3 are
  templates marked with a `Template` tag. Replace the copy, fill the `slot` metric values in the
  side panel, then delete the `.note` paragraph once all three are real.
- **Path** — the `<div class="path">` timeline. Fill the `20XX` roles.
- **Résumé** — the "Résumé — PDF" links point to `#`. Drop a `resume.pdf` in `public/` and point
  the `href` at `/resume.pdf`.

## Deploy

Every push to `main` deploys to production on Vercel. Pushes to other branches get a preview URL.
