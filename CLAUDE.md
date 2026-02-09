# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal website for William Whittenton, hosted on GitHub Pages at **whittenton.us**. The entire site is a single `index.html` file with inline CSS — no build tools, no JavaScript, no dependencies.

## Architecture

- **index.html** — The complete site: markup, styling (via `<style>` block), and content. Uses CSS custom properties for theming with automatic light/dark mode via `prefers-color-scheme`.
- **CNAME** — Custom domain configuration for GitHub Pages (`whittenton.us`).
- **resume.pdf** — Downloadable resume, linked from the site.

## Deployment

Pushing to `main` triggers GitHub Pages deployment automatically. There is no build step — the static files are served directly.

## Development

No install, build, lint, or test commands. Open `index.html` in a browser to preview changes locally.

## Key Design Patterns

- All styling is inline in the `<style>` block — no external CSS files. CSS variables defined in `:root` control the color scheme.
- Dark mode is handled entirely through `@media (prefers-color-scheme: dark)` overriding the CSS custom properties.
- The layout uses a single `.container` with `max-width: 800px`. Responsive breakpoint at 640px.

## Git Conventions

- Do not include `Co-Authored-By` trailers in commit messages.
