# AGENTS.md

This file provides guidance to AI coding agents (Claude Code, Codex, Cursor, …) working in this repository.

## Project Overview

TICORI LLC company website, hosted on GitHub Pages at www.ticori.gg. This is an indie game development studio's static site with a landing page and press kit.

## Architecture

- **Static HTML site** — no build system, framework, or bundler. All CSS is inline within each HTML file.
- `index.html` — Main landing page with mystery/coming-soon game teaser
- `press-kit.html` — Studio factsheet, logo downloads and brand colours
- `brand/` — logo files and favicons
- `CNAME` — Custom domain configuration (www.ticori.gg)
- `.gitignore` — Configured for Jekyll/GitHub Pages (though site currently uses plain HTML)

## Development

No build or test commands. Open HTML files directly in a browser to preview. Deploy by pushing to `main` — GitHub Pages serves automatically.

## Git

- Do not add `Co-Authored-By` lines to commits.

## Style Conventions

- Palette ("Game night", v4 brand): page background `#231A15` (ink), raised surfaces `#2E241E`, headings and the logo `#FFF4E6` (cream), body text `#D3C8BC`, muted `#9C9288`, `#FF5A36` (tomato) only for the mark's accents, links and the one main button, hover `#FF7A5C`; sun `#FFC93C` and teal `#1FA89A` appear only in the press kit palette
- Naming: "Ticori" in running text, the lowercase `ticori` only as the wordmark image, "TICORI LLC" only where the legal entity is meant (copyright, factsheet)
- Typography: Fredoka 500/600 for headings (the closest real font to the lowercase `ticori` wordmark), Nunito 400 to 800 for body; sentence case everywhere, no all-caps labels
- Layout (home page): ink hero with the splash, then a full-width tomato "tabletop" bar as the one divider, a cream games band (Steam widget left, text right, no card), an ink promise band, and the footer, where the cream mark rests its paws on a tabletop bar aligned to its own table (`.peek-row`)
- Logo: the v4 jackalope at the table and the lowercase `ticori` wordmark (tomato i-dots), raster PNGs copied from the branding repo's `v4/` into `brand/`, `cream` on the site's dark backgrounds (it matches the cream text), `ink` on light, `white` only as a press-kit download (pure white is for the game splash, beside white middleware logos); only the current logo belongs in this public repo. The home page hero is the splash built from the three `splash_*_cream.png` sprites (one shared 600x520 frame, cropped in CSS): the paws and the table are shown, the head rises from behind the table (clipped at 55.19% of the frame) in one 450 ms ease-out-back motion, then the wordmark fades in, with the brand's `splash_layout.txt` timing; it plays once per session, any click or key skips it, and it is skipped under `prefers-reduced-motion` or in a background tab, with a timer that always reveals the page
- Content: home is the studio line, then the games (each with the three promise lines next to the store widget), then About (the story, then the Promise); the footer carries "Online games for friends. Played fair."
- Dark theme with grain texture overlay (SVG feTurbulence data URI on `body::after`) and a faint cream radial glow at the top of the body background
- CSS custom properties in `:root` define the palette; shared visual style is duplicated across HTML files (no shared CSS file)
- Responsive with a 768px mobile breakpoint; hero uses staggered load animation with `prefers-reduced-motion` fallback
