# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of standalone HTML prototypes and demos. Each file is self-contained with embedded CSS and vanilla JavaScript — no build step, no package manager, no framework.

## Development Servers

**Root directory** (serves all HTML files):
```
npx serve -p 3000 .
```

**nc500 subdirectory** (Python server):
```
python3 -m http.server 3456
```

## Architecture

All files are single-file HTML apps with inlined CSS and JS. No external build tools or transpilation.

### Files

- **credit-portal.html** — "LoanPilot" enterprise finance portal; petrol/yellow color scheme; vanilla JS for expand/collapse task groups
- **dashboard.html** — "Nexus" dark-mode analytics dashboard; Canvas 2D API for revenue charts (MRR/ARR); purple/cyan accent colors
- **eggs.html** — Egg nutrition facts page; integrates the Figma MCP capture script (`mcp.figma.com`) for sending elements to Figma designs
- **nc500/index.html** — NC500 Scottish cycling route; uses Leaflet.js (CDN) with 150+ hardcoded waypoints; companion GPX file at `nc500/nc.gpx` (komoot export, 1.1 MB)

### External Dependencies (CDN only)

- **Leaflet.js v1.9.4** — used in nc500/index.html for interactive maps
- **Figma MCP capture script** — used in eggs.html for Figma integration

## No Tests or CI

There are no tests, linters, or CI pipelines configured in this project.
