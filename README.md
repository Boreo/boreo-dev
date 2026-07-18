# boreo.dev

Personal site. One page, static Astro build, no client framework. All content lives in `src/data/site.ts`, so changing text, links or certifications never touches markup. Theme is Catppuccin Mocha.

The background is a canvas constellation: a jittered grid of dots with distance-faded edges, cursor repel, and an occasional shooting star. The glows and card shadow are pre-rendered per pixel with dither because plain CSS gradients band badly on dark backgrounds. The animation loop stops when nothing is moving and everything respects `prefers-reduced-motion`.

## Structure

```
.
├── astro.config.mjs
├── package.json
├── public/
│   ├── favicon.svg
│   ├── microsoft-certified-associate-badge.svg
│   └── og.png
└── src/
    ├── data/
    │   └── site.ts        content: profile, links, certifications
    └── pages/
        └── index.astro    the whole page: markup, script, styles
```

## Commands

| Command | Action |
| --- | --- |
| `npm run dev` | local dev server |
| `npm run build` | static build to `dist/` |
| `npm run preview` | serve the build |
