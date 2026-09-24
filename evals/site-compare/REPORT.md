# rangka-skill.vercel.app vs splicecraft.vercel.app

Date: 2026-09-25. Captures: `*-first.png` / `*-full.png` at 390x844 and 1440x900, light and dark (Playwright, Chromium). Raw numbers: `metrics.json`. Post-fix captures: `rangka-new-*.png`.

## Scorecard

| Criterion | Rangka | Splicecraft | Winner | Evidence |
|---|---|---|---|---|
| First-screen clarity | 9 | 9 | tie | Both: one strike/replace headline plus a live product mockup. Rangka mobile used to push the CTA below the fold; fixed, CTA now ends at y<=412 of 844 in all 6 languages. Splicecraft still shows the install command in the first screen, which Rangka does not. |
| Typography | 9 | 8 | Rangka | Fraunces + Inter + JetBrains Mono, self-hosted with preload; editorial serif headline. Splicecraft's tight grotesk is strong but letter-spacing collides at 1440. |
| Visual richness | 8 | 9 | Splicecraft | Splicecraft's phone mockup with animated captions is more vivid than Rangka's document mockup. Rangka adds campus chips and a closing wordmark but stays quieter by design. |
| Motion | 8 | 8 | tie | Both animate the hero; Rangka respects prefers-reduced-motion. |
| Mobile layout | 9 | 8 | Rangka | No horizontal overflow in 24/24 Rangka configs; headline sizing is per-language. |
| i18n | 10 | 6 | Rangka | Rangka: id, en, es, fr, zh, ar (RTL). Splicecraft: EN/ID only. |
| Theme | 10 | 5 | Rangka | Rangka: light/dark/system toggle, no flash. Splicecraft rendered light under `prefers-color-scheme: dark`. |
| Performance | 9 | 7 | Rangka | Transfer 176 KB vs 1026 KB; warm FCP ~0.53 s vs ~0.56-0.64 s. Rangka's cold first run at 390 showed CLS 0.17 (font swap); fonts are now self-hosted with `font-display: optional` and preload. |
| Accessibility | 9 | 6 | Rangka | axe: 0 violations on Rangka; Splicecraft 3-4 rules incl. color-contrast on ~75 nodes. Rangka's scrollable tables/pre got `tabindex=0`; `--wait` darkened for contrast. |

Rangka wins 6, ties 2, loses 1 (visual richness).

## Fixes in this pass
- Mobile hero: CTA moved directly under the headline, before the product mockup; mockup capped at 220px.
- Kept the previous agent's uncommitted work after review: self-hosted fonts, build-time stats from `references/` and `evals/` (`src/data.js`), campus chips, footer wordmark, a11y tabindex fixes, font cache headers, i18n keys `stat5-8`/`cam_src`/`cam_lead` (id inline + en/es/fr/zh/ar packs all complete).

## Re-test (built `dist/`)
390x844 and 1440x900 x light/dark x id/en/es/fr/zh/ar = 24 runs: scrollWidth <= viewport and 0 console errors in all 24; `ar` renders `dir=rtl`.
