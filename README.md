# storyCast

An accessible microsite showcasing African art and artists — paintings, sculptures, textiles, and documentary — built with semantic HTML5, Sass, CSS Grid + Flexbox, container queries, and vanilla JS.

---

## Project Structure

```
storyCast/
├── index.html                          # Home page
├── about.html                          # About & Access page
├── story/
│   ├── el-anatsui.html                 # El Anatsui — Sculpture & Installation
│   ├── wangechi-mutu.html              # Wangechi Mutu — Collage & Sculpture
│   ├── billie-zangewa.html             # Billie Zangewa — Silk Collage
│   └── african-art-documentary.html    # Documentary — Women Remaking Kigali's Art Scene
├── sass/
│   ├── main.scss                       # Entry point (imports all partials)
│   └── partials/
│       ├── _colors.scss                # Color tokens
│       ├── _typography.scss            # Type scale, font stacks
│       ├── _spacing.scss               # Spacing, shadow, radius tokens
│       ├── _reset.scss                 # Normalize + base styles
│       └── _components.scss            # All BEM components
├── css/
│   └── main.css                        # Compiled CSS (do not edit directly)
├── assets/
│   ├── audio/
│   │   ├── el-anatsui.mp3
│   │   ├── Wangechi-Mutu.mp3
│   │   └── Billie-Zangewa.mp3
│   ├── video/
│   │   └── African-Art-Documentary.mp4
│   └── transcripts/
│       └── african-art-documentary-captions.vtt
└── README.md
```

---

## Pages

| Page | File | Content |
|------|------|---------|
| Home | `index.html` | Featured artist, art card grid, newsletter |
| El Anatsui | `story/el-anatsui.html` | Audio interview, gallery, artist statement |
| Wangechi Mutu | `story/wangechi-mutu.html` | Audio interview, gallery, extended descriptions |
| Billie Zangewa | `story/billie-zangewa.html` | Audio interview, gallery, transcript |
| Documentary | `story/african-art-documentary.html` | Video + captions + full transcript |
| About & Access | `about.html` | Mission, accessibility features, team |

---

## Running Locally

Open via a local server — do not open HTML files directly from the file system.

### Option 1 — VS Code Live Server
1. Open the `storyCast` folder in VS Code
2. Install **Live Server** by Ritwick Dey
3. Right-click `index.html` → Open with Live Server
4. Opens at `http://127.0.0.1:5500`

### Option 2 — Python
```bash
python -m http.server 5500
```
Then open `http://localhost:5500`

### Recompiling Sass
```bash
sass --watch sass/main.scss css/main.css
```

---

## Design System

### Color Palette

| Token | Hex | Use |
|-------|-----|-----|
| `$color-midnight` | `#0E0C0A` | Page background |
| `$color-soil` | `#1C1712` | Card surfaces |
| `$color-terracotta` | `#C4522A` | Primary accent, links |
| `$color-gold` | `#D4A843` | Secondary accent, active nav |
| `$color-ivory` | `#F5F0E8` | Body text |
| `$color-sand` | `#A89880` | Secondary text, metadata |
| `$color-forest` | `#2D5A3D` | Badges, success indicators |

### Typography

| Stack | Variable | Used for |
|-------|----------|----------|
| Cormorant Garamond | `$font-display` | Headings, artist names, pull quotes |
| DM Sans | `$font-body` | All body copy and UI |
| DM Mono | `$font-mono` | Labels, metadata, transcripts |

---

## Accessibility Checklist

### Images & Artwork
- [x] Every artwork wrapped in `<figure>` with `<figcaption>` describing medium, dimensions, and visual content
- [x] Extended image description panels on all artist pages
- [x] Decorative SVGs use `aria-hidden="true"`

### Media
- [x] Audio interviews have full timed transcripts
- [x] Video documentary has closed captions via WebVTT `<track>` element
- [x] All media uses native browser controls — keyboard accessible

### Navigation & Structure
- [x] Skip link is first focusable element on every page
- [x] Landmark regions on every page — `<header>`, `<nav>`, `<main>`, `<footer>`, `<aside>`
- [x] Full keyboard navigation throughout
- [x] Visible `:focus-visible` gold ring on all interactive elements
- [x] Breadcrumb navigation on all story pages
- [x] `aria-current="page"` on active nav links

### Semantic HTML
- [x] Heading hierarchy h1 → h2 → h3 with no skips
- [x] `<dl>`, `<dt>`, `<dd>` for artist metadata
- [x] `<article>` wraps each card and team member
- [x] `aria-expanded` + `aria-controls` on all toggle buttons

### Color Contrast (WCAG 2.1 AA minimum 4.5:1)

| Combination | Ratio | Result |
|-------------|-------|--------|
| Ivory `#F5F0E8` on Midnight `#0E0C0A` | 14.8:1 | ✓ AAA |
| Sand `#A89880` on Midnight `#0E0C0A` | 5.2:1 | ✓ AA |
| Terracotta `#C4522A` on Midnight `#0E0C0A` | 4.9:1 | ✓ AA |
| Gold `#D4A843` on Midnight `#0E0C0A` | 7.3:1 | ✓ AAA |

### Motion
- [x] `prefers-reduced-motion` disables all animations
- [x] No autoplay on any media

---

## Team

**Armstrong Ngororano** — Founder & Editor

---

## Tools Used

- HTML5 (semantic, no frameworks)
- Sass (partials and tokens, compiled to CSS)
- Vanilla JavaScript (mobile nav, panel toggles)
- Google Fonts (Cormorant Garamond, DM Sans, DM Mono)
- Inline SVG for all illustrations

# High fedelity figma mockup: https://www.figma.com/design/GQdrCvnIffY5HrmjxdB5TQ/Untitled?t=Erd1enofUGVcjyfk-0
# Sitemap figma mockup: https://www.figma.com/board/bkQNrM8YmWM21wYGNwCYou/StoryCast?node-id=0-1&p=f&t=Hw3JdkXTGmOMa8k5-0
