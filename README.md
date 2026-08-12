# alpgiraykocal.com

Personal landing page — a hub pointing to my LinkedIn profile and live projects.

## Stack

Single static `index.html`. No build step, no dependencies, no framework.
Served by GitHub Pages from the `main` branch root.

## Structure

| File | Purpose |
|------|---------|
| `index.html` | The entire page: markup, inlined CSS tokens, and a small vanilla-JS block for theme, language and entrance animations |
| `CNAME` | Custom domain for GitHub Pages (`alpgiraykocal.com`) |
| `.nojekyll` | Skips Jekyll processing |
| `robots.txt`, `sitemap.xml` | Basic indexing hints |

## Design notes

- **Style:** minimalism / Swiss grid, dark-first with a full light theme
- **Type:** Inter for UI text, JetBrains Mono for labels and metadata
- **Theme:** follows `prefers-color-scheme`, overridable by the toggle, stored in `localStorage`
- **Language:** EN/TR toggle driven by `[data-i18n-en]` / `[data-i18n-tr]` attributes and the `lang` attribute on `<html>`
- **Accessibility:** skip link, visible focus rings, 44px+ touch targets, `prefers-reduced-motion` respected, WCAG AA contrast in both themes

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.
