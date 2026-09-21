# AGENTS.md

This file provides guidance to AI coding agents (Claude Code, Codex, Cursor, …) working in this repository.

## Project Overview

TICORI LLC company website, hosted on GitHub Pages at www.ticori.gg. This is an indie game development studio's static site with a landing page and press kit.

## Architecture

- **Static HTML site** — no build system, framework, or bundler. All CSS is inline within each HTML file.
- `index.html` — Main landing page with mystery/coming-soon game teaser
- `press-kit.html` — Studio factsheet and press information
- `CNAME` — Custom domain configuration (www.ticori.gg)
- `.gitignore` — Configured for Jekyll/GitHub Pages (though site currently uses plain HTML)

## Development

No build or test commands. Open HTML files directly in a browser to preview. Deploy by pushing to `main` — GitHub Pages serves automatically.

## Git

- Do not add `Co-Authored-By` lines to commits.

## Style Conventions

- Palette ("Folklore Dark"): background `#141210` (char), raised surfaces `#1c1916`, headings/text `#ede7d9` (bone), body text `#b5ad9b`, muted `#7d7768`, accent `#8aa86f` (moss), accent hover `#a4c186`
- Typography: Fraunces (display serif, headings/wordmark), Work Sans (body), IBM Plex Mono (uppercase micro-labels, `.mono` class)
- Dark theme with grain texture overlay (SVG feTurbulence data URI on `body::after`) and a moss-tinted radial glow in the body background
- CSS custom properties in `:root` define the palette; shared visual style is duplicated across HTML files (no shared CSS file)
- Responsive with a 768px mobile breakpoint; hero uses staggered load animation with `prefers-reduced-motion` fallback
