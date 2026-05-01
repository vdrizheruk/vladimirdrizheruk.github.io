# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-page personal portfolio / CV for Vladimir Drizheruk, hosted on GitHub Pages at `https://vladimir.drizheruk.name/` (CNAME). There is no build step, no package manager, and no test suite — `index.html` is served directly as-is.

## Deploying

Push to `master` → GitHub Pages serves it automatically. There is nothing to build or compile.

## Architecture

Everything lives in one file: [index.html](index.html).

- **CSS** — fully inline inside `<style>`. Uses CSS custom properties (`--gold`, `--muted`, `--line`, etc.) defined in `:root` for the colour palette. Single responsive breakpoint at `900px`.
- **JS** — a single small `<script>` at the end of `<body>`, only wires up the mobile hamburger menu toggle.
- **Sections** (in order): hero → `#expertise` → `#impact` → `#experience` → `#technology` → `#contact`.
- **SEO / meta**: canonical URL, Open Graph, Twitter Card, and a JSON-LD `Person` schema are all in `<head>`.

## Key content conventions

- The colour palette token is `--gold` / `--gold-2` (amber accent) and `--muted` (secondary text).
- Technology tags use `.tag` inside `.taglist`; section cards use `.card` inside `.grid-2` or `.grid-3`.
- Timeline entries use `.role` with a `<time datetime="YYYY">` for the date column.
- The portrait image is `vladimir-drizheruk-executive-portrait.png` (served from repo root).
