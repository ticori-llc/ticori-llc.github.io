# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

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

- Brand color: `#58b08d` (green), hover accent: `#6dd5b4`
- Dark theme with glassmorphism (backdrop-filter blur, semi-transparent backgrounds)
- Shared visual style is duplicated across HTML files (no shared CSS file)
- Responsive with a 768px mobile breakpoint
