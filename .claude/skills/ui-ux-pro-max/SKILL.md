# UI/UX Pro Max — Design Intelligence Skill

> AI-powered design intelligence system providing professional-grade UI/UX guidance.
> Adapted from: github.com/nextlevelbuilder/ui-ux-pro-max-skill

## Core Design Database

- **67 UI styles**: Glassmorphism, Claymorphism, Brutalism, Neumorphism, Aurora UI, Dark Mode OLED, Bento Box Grid, Swiss Modernism 2.0, HUD/Sci-Fi FUI, Editorial Grid, Cyberpunk UI, etc.
- **96 color palettes**: Industry-specific (Finance, Healthcare, Tech, Government, etc.)
- **57 font pairings**: Google Fonts optimized combinations
- **100 UX reasoning rules**: Industry-specific design logic
- **25 chart types**: Data visualization best practices

## Supported Stacks

React, Next.js, Vue, Svelte, Tailwind CSS, shadcn/ui, SwiftUI, React Native, Flutter, Jetpack Compose, HTML+CSS (vanilla)

## Design Priority Framework (Highest → Lowest)

1. **Accessibility** (CRITICAL)
   - Minimum 4.5:1 contrast ratio for normal text
   - Minimum 3:1 for large text (18px+ or 14px+ bold)
   - ARIA labels on all interactive elements
   - Keyboard navigation support
   - `prefers-reduced-motion` respect

2. **Touch & Interaction** (CRITICAL)
   - Minimum 44x44px touch targets
   - `cursor: pointer` on ALL clickable elements
   - Smooth transitions 150–300ms
   - Hover states on desktop, active states on mobile
   - Focus-visible outlines (never remove, restyle instead)

3. **Performance**
   - Lazy load images below the fold
   - `font-display: swap` for web fonts
   - Prefer CSS animations over JS (use `transform` and `opacity`)
   - Avoid layout shifts (CLS < 0.1)

4. **Layout**
   - Mobile-first responsive design
   - CSS Grid for 2D layouts, Flexbox for 1D alignment
   - Max content width: 1200–1440px
   - Consistent spacing scale (4px base: 4, 8, 12, 16, 24, 32, 48, 64)

5. **Typography & Color**
   - Maximum 2 font families per project
   - Type scale: 12, 14, 16, 18, 20, 24, 32, 40, 48, 64px
   - Line height: 1.4–1.6 for body, 1.1–1.3 for headings
   - Color: dominant + accent pattern (not evenly distributed)
   - Dark mode: test all colors in both themes

6. **Animation & Motion**
   - One well-orchestrated page load > scattered micro-interactions
   - Staggered reveals for lists (50ms delay increment)
   - Ease-out for entrances, ease-in for exits
   - Duration: 150ms for micro, 300ms for transitions, 500ms for page-level

7. **Style Selection**
   - Match style to industry and audience
   - Finance/Government: authoritative, data-dense, dark themes
   - Consumer: approachable, vibrant, rounded corners
   - Developer tools: terminal aesthetic, monospace, high information density

## Professional Rules (Non-Negotiable)

- NO emojis as functional icons — use SVG or icon libraries
- NO placeholder images in production — use real content or shimmer loaders
- NO horizontal scroll on mobile (except carousels/tables)
- NO text smaller than 12px on mobile
- NO unclickable elements that look clickable
- `cursor: pointer` on ALL interactive elements
- Sufficient contrast in BOTH light and dark modes
- Loading states for ALL async operations
- Error states for ALL form fields
- Empty states for ALL list views

## Finance/Government Sector Specific Guidelines

For career dashboards, financial analysis tools, and government-related UIs:

### Color Palette
```
Background: #06080e → #0c0f1a → #111628 (deep navy-black layers)
Cards: #131831 → #1a2040 → #212850 (elevated surfaces)
Borders: #1c2548 → #283260 (subtle definition)
Text: #e8ecf4 (primary), #8899b8 (secondary), #506080 (tertiary)
Accent: #4a90e8 (blue), #9066f0 (purple), #e8a020 (gold)
Status: #20c860 (positive), #e84444 (negative), #f07020 (warning)
```

### Typography
- Display: **Sora** (800 weight, tight letter-spacing)
- Body: **Noto Sans KR** (400/500/700 for Korean)
- Data: **JetBrains Mono** (monospace for scores/numbers)

### Layout Pattern
- Bento grid for overview stats
- Data tables with sticky headers
- Expandable rows for detail views
- Grade/tier badge system with gradient backgrounds
- Numbered section headers (01, 02, 03...)

## Pre-Delivery Checklist

Before finalizing any UI work:
- [ ] All interactive elements have `cursor: pointer`
- [ ] Contrast ratios pass WCAG AA (4.5:1 body, 3:1 large)
- [ ] Responsive at 320px, 768px, 1024px, 1440px
- [ ] Loading/error/empty states exist
- [ ] Transitions are smooth (no jank)
- [ ] Dark mode colors verified
- [ ] Touch targets >= 44px
- [ ] No horizontal overflow on mobile
- [ ] Font loading optimized (`font-display: swap`)
- [ ] Keyboard navigation works for all interactive elements
