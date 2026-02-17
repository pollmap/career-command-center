# Frontend Design — Distinctive UI Creation Skill

> Guides creation of distinctive, production-grade frontend interfaces.
> Adapted from: github.com/anthropics/skills (frontend-design)

## Core Philosophy

**Avoid "AI slop" design.** The default output of most AI tools produces generic, forgettable interfaces — purple gradients on white, rounded cards with shadows, and cookie-cutter layouts. This skill exists to break that pattern.

## Before Writing Any Code

Analyze context across four dimensions:

1. **Purpose & Audience** — Who uses this? What do they need to accomplish?
2. **Tone Commitment** — Pick an extreme and commit:
   - Brutally minimal
   - Maximalist chaos
   - Retro-futuristic
   - Bloomberg terminal
   - Editorial magazine
   - Dark terminal + finance hybrid
3. **Technical Constraints** — What stack? What browsers? What devices?
4. **Differentiation** — What makes this UNFORGETTABLE?

## Design Pillars

### Typography — The #1 Differentiator
- **AVOID**: Generic fonts (Arial, Helvetica, basic Inter, default system fonts)
- **SEEK**: Unexpected, characterful font choices
- **PAIR**: Maximum 2–3 families with clear hierarchy
- Good pairings for financial/technical UIs:
  - **Sora** (display) + **Noto Sans KR** (body) + **JetBrains Mono** (data)
  - **Bebas Neue** (headlines) + **Inter** (body) + **IBM Plex Mono** (code)
  - **Space Grotesk** (display) + **DM Sans** (body) + **Fira Code** (data)
- Letter-spacing: tight (-0.5px to -1.5px) for large display text
- Font weight contrast: 800–900 for headings, 400 for body

### Color — Bold, Not Timid
- **AVOID**: Evenly distributed rainbow palettes, pastel everything
- **SEEK**: One dominant tone with sharp accents
- Dark UIs: layer backgrounds in 3+ shades (not just #000 and #111)
- Light UIs: use warm whites (#fafafa, #f8f7f4) not pure white (#fff)
- Financial data: red/green for loss/gain, gold for emphasis, blue for neutral
- Gradients: subtle, directional, used sparingly (135deg preferred)

### Motion — Choreographed, Not Scattered
- **AVOID**: Random micro-interactions on every element
- **SEEK**: One well-orchestrated page load with staggered reveals
- Entrance: items cascade in with 50ms delays
- Scroll: parallax only if it serves the narrative
- Hover: subtle scale (1.02) or background shift, not dramatic bounces
- Transitions: `cubic-bezier(0.4, 0, 0.2, 1)` for natural easing

### Layout — Break the Grid (Intentionally)
- **AVOID**: Perfect symmetry, identical card sizes, uniform spacing
- **SEEK**: Asymmetry, overlap, diagonal flow, grid-breaking hero elements
- Bento grids: varying cell sizes (1x1, 2x1, 1x2, 2x2)
- Sticky elements: headers, sidebars, navigation
- Z-index layers: background → content → navigation → overlays → modals
- Whitespace: generous, intentional, part of the design

### Backgrounds — Build Atmosphere
- **AVOID**: Flat solid colors
- **SEEK**: Gradients, noise textures, layered transparencies, grain overlays
- Subtle `background-blend-mode` effects
- CSS noise: `url("data:image/svg+xml,...")` for texture
- Layered backgrounds with varying opacity
- For dark themes: deep navy-black (#06080e) not pure black (#000)

## Explicit Prohibitions

1. No "overused font families" — if you've seen it on 100 websites, skip it
2. No "purple gradients on white backgrounds" — the #1 AI slop tell
3. No "cookie-cutter design" — if swapping the logo makes it unrecognizable, start over
4. No centered-everything layouts — alignment should be intentional
5. No default shadows — if using shadows, customize them (color, spread, offset)

## Design Reference: CUFA (cufa-web.vercel.app)

This project's design reference is the CUFA website, which embodies:
- **Dark terminal + editorial finance** aesthetic (Bloomberg meets developer tooling)
- **Bebas Neue** condensed display font for headlines
- **Numbered sections** (01, 02, 03) with clear vertical flow
- **High-contrast monochrome** with minimal color accents
- **Terminal simulation** with `$` prompt styling
- Small pill badges for tags/labels
- Serious, institutional, technically sharp tone

### Apply These CUFA Principles:
- Section numbers as design elements (large, contrasting)
- Code/terminal aesthetic for data-heavy sections
- Minimal but confident use of accent colors
- Condensed, uppercase labels for section headers
- Grid-based layouts with varying density
- Full-width sections with contained content

## Guiding Philosophy

Match code complexity to vision:
- **Minimalism** needs precision — every pixel matters
- **Maximalism** needs elaborate effects — go all in
- **Data-dense UIs** need hierarchy — size, weight, color, position all carry meaning

The goal is not "pretty" — the goal is **memorable, functional, and distinctly yours**.
