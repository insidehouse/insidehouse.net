# CLAUDE.md

## Project Overview

**insidehouse.net** is a personal/team digital hub - a landing page that serves as a central gateway to various subdomains and projects. The site is designed as a minimal, dark-themed single-page website in Traditional Chinese.

## Tech Stack

- **Static HTML/CSS**: Single `index.html` file with embedded styles
- **Hosting**: GitHub Pages with custom domain (insidehouse.net)
- **No build process**: Edit and deploy directly

## Project Structure

```
/
├── CNAME          # Custom domain configuration for GitHub Pages
├── index.html     # Main (and only) page - contains all HTML, CSS, and JS
└── CLAUDE.md      # This file
```

## Design System

CSS custom properties defined in `:root`:
- `--bg`: #0b0b0c (background)
- `--panel`: #121214 (panel background)
- `--text`: #e9e9ee (primary text)
- `--muted`: #a7a7b3 (secondary text)
- `--line`: rgba(255,255,255,.10) (borders)
- `--radius`: 18px (border radius)
- `--max`: 1040px (max content width)

## Key Components

- **Hero section**: Main introduction with CTAs
- **Card grid**: 12-column grid with `.half` (6-col) and `.third` (4-col) variants
- **Navigation pills**: Rounded pill-style nav links
- **Tags/Links**: Small interactive elements within cards

## Development Notes

- All styles are inline in `<style>` tag - no external CSS
- Responsive breakpoint at 860px
- Font stack prioritizes system fonts with CJK fallbacks (Noto Sans TC, PingFang TC, etc.)
- Minimal JavaScript: only auto-updates copyright year

## Sections

1. **Lab** - Experiments and quick pages
2. **Docs** - Reports, proposals, notes
3. **Projects** - Selected works
4. **About** - Introduction and contact
5. **Now** - Current status/focus

## Common Tasks

### Adding a new card
Add inside `.grid` section using the card template:
```html
<article class="card half">  <!-- or "card third" -->
  <h2>Title</h2>
  <p>Description</p>
  <div class="links">
    <a class="tag" href="#"><strong>Label</strong> <small>subtitle</small></a>
  </div>
</article>
```

### Updating links
Replace `href="#"` placeholders with actual URLs (e.g., `https://lab.insidehouse.net`)

## Language

Primary content is in **Traditional Chinese (zh-Hant)**. Keep UI text consistent with existing tone.
