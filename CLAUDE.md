# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a wedding website built with Nuxt 4 and Vue 3. The project uses TypeScript and follows Nuxt 4's `/app/` directory convention.

## Development Commands

```bash
npm run dev       # Start development server on http://localhost:3000
npm run build     # Build for production
npm run generate  # Generate static site
npm run preview   # Preview production build locally
```

## Architecture

- **Framework**: Nuxt 4.3.0+ with Vue 3.5
- **Entry Point**: `app/app.vue` is the root Vue component
- **Static Assets**: `public/` directory (images in `public/image/`)
- **Configuration**: `nuxt.config.ts` with devtools enabled

## Notes

- No testing or linting tools are currently configured
- Uses ES modules (`"type": "module"`)
- Wedding photos stored in `public/image/` (1.jpg through 4.jpg)
