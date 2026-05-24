# AGENTS.md

This document provides an overview of the project structure for AI agents working on this codebase.

## Project Overview

A3 Rocket Consulting marketing site built with TanStack Start, deployed on Netlify.

### Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | TanStack Start |
| Frontend | React 19, TanStack Router v1 |
| Build | Vite 7 |
| Styling | Tailwind CSS 4 |
| Language | TypeScript 5 (strict mode) |
| Deployment | Netlify |

## Directory Structure

```
├── public/             # Static assets (favicon, images)
├── src/
│   ├── data/
│   │   └── products.ts # Service/product catalog data
│   ├── routes/
│   │   ├── __root.tsx  # Root layout, HTML shell, global head config
│   │   ├── index.tsx   # Home page / marketing landing
│   │   └── products/
│   │       └── $productId.tsx  # Individual product/service detail page
│   ├── router.tsx      # TanStack Router setup
│   └── styles.css      # Global styles (Tailwind)
├── netlify.toml        # Netlify build config
├── package.json
├── tsconfig.json
└── vite.config.ts
```

## Key Concepts

### File-Based Routing
Routes are defined by files in `src/routes/`. The `__root.tsx` wraps all pages with the HTML shell.

### Branding
- Site title: "A3 Rocket Consulting" — set in `src/routes/__root.tsx` head config
- Page heading: set in `src/routes/index.tsx`

## Development Commands

```bash
npm run dev    # Start dev server on port 3000
npm run build  # Production build
```

## Conventions
- Components: PascalCase
- Routes: file-based, kebab-case files
- Styling: Tailwind CSS utility classes
- TypeScript strict mode, `@/` alias for `src/`
