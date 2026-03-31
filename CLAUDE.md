# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of standalone HTML prototypes and demos. Each file is self-contained with embedded CSS and vanilla JavaScript — no build step, no package manager, no framework.

## Development Server

```
npx serve -p 3000 .
```

## Architecture

All files are single-file HTML apps with inlined CSS and JS. No external build tools or transpilation.

### Files

- **gps-merge/index.html** — "TrailMerge" GPX track merger; forest/green color scheme; Leaflet.js map with drag-and-drop GPX upload, client-side XML parsing, track merging; test GPX fixtures in `gps-merge/test-track-{a,b,c}.gpx`
- **contact-test/contact.html** — Contact form UI; Inter + Indie Flower fonts (Google Fonts CDN); light grey background layout

### External Dependencies (CDN only)

- **Leaflet.js v1.9.4** — used in gps-merge/index.html for interactive maps
- **Figma MCP capture script** (`mcp.figma.com`) — included in both files for sending elements to Figma designs
- **Google Fonts** — Inter + Indie Flower used in contact-test/contact.html

## No Tests or CI

There are no tests, linters, or CI pipelines configured in this project.
