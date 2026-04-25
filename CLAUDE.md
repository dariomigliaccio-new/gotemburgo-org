# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Static landing page for the inauguration of the first AD-Belém congregation in Gothenburg, Sweden (25 April 2026). Hosted on GitHub Pages at **gotemburgo.org**.

## Deployment

Push to `main` → GitHub Pages rebuilds automatically. The `CNAME` file sets the custom domain to `gotemburgo.org`. DNS is managed on **GoDaddy**, pointing to GitHub Pages.

- GitHub repo: `github.com/dariomigliaccio-new/gotemburgo-org`
- No build step, no CI pipeline.

## Architecture

Single-file site: everything lives in `index.html` — HTML structure, all CSS (embedded `<style>`), and a tiny inline `<script>` (copy-link button). No frameworks, no bundler.

**CSS design tokens** (`:root` variables):
- `--gold: #c9a84c` — accent color throughout
- `--dark: #12182b` — dark section backgrounds
- `--cream: #f5f0e8` — light section backgrounds

**Fonts** (Google Fonts, loaded in `<head>`):
- `Cinzel` — headings, labels, badges
- `EB Garamond` — body text

**Page sections** (in order): Hero → Ao Vivo → Data Strip → História → Evento → Compartilhe → Footer

## Images

All images sit at the repo root alongside `index.html`:

| File | Used for |
|---|---|
| `gotemburgo_1916.jpg` | Hero background |
| `pastor.jpg` | Pastor circle photo in hero |
| `fundadores_bg.jpg` | Founders photo in História section |
| `gotemburgo_1900.jpg` | Available but not currently used |
| `1secao.png` | Available but not currently used |

Images are referenced with bare filenames (no path prefix) — keep them at the root.
