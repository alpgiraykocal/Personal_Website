# alpgiraykocal.com

Personal landing page — a hub pointing to my LinkedIn profile and the experiments I keep live.

## Stack

Single static `index.html`. No build step, no dependencies, no framework.
Served by GitHub Pages from the `main` branch root.

## Structure

| File | Purpose |
|------|---------|
| `index.html` | The entire page: markup, inlined CSS tokens, and a small vanilla-JS block for theme and entrance animations |
| `CNAME` | Custom domain for GitHub Pages (`alpgiraykocal.com`) |
| `.nojekyll` | Skips Jekyll processing |
| `og.png` | 1200×630 social preview card, rendered from the site's own type and colours |
| `apple-touch-icon.png` | 180×180 home-screen icon |
| `robots.txt`, `sitemap.xml` | Basic indexing hints |

## Design notes

- **Style:** minimalism / Swiss grid, dark-first with a full light theme
- **Type:** Inter for UI text, JetBrains Mono for labels and metadata
- **Theme:** follows `prefers-color-scheme`, overridable by the toggle, stored in `localStorage`. Resolved by an inline script in `<head>` so there is no flash of the wrong theme before first paint
- **Language:** English only
- **Accessibility:** skip link, visible focus rings, 44px+ touch targets, `prefers-reduced-motion` respected, WCAG AA contrast in both themes, external links announce that they open a new tab
- **Resilience:** the entrance animation is gated behind a `.js` class, so the page renders fully with scripting disabled
- **Layout stability:** a metric-matched `@font-face` fallback stands in for Inter while it loads, so the swap doesn't reflow the page

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
