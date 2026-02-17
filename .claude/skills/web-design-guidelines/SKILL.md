# Web Design Guidelines — Audit & Best Practices Skill

> Audits UI code against 100+ rules covering accessibility, performance, and UX.
> Adapted from: github.com/vercel-labs/agent-skills (web-design-guidelines)

## Trigger Phrases

Activate this skill when asked to: "Review my UI", "Check accessibility", "Audit the design", "Improve UX", "Fix design issues"

## Audit Categories

### 1. Accessibility (WCAG AA Minimum)

- [ ] All `<img>` have meaningful `alt` text (not "image" or "photo")
- [ ] All `<button>` have accessible names (text content or `aria-label`)
- [ ] All `<input>` have associated `<label>` elements
- [ ] Color contrast: 4.5:1 for normal text, 3:1 for large text
- [ ] No information conveyed by color alone (use icons/text too)
- [ ] `lang` attribute on `<html>` element
- [ ] Semantic HTML: `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`
- [ ] Skip-to-content link for keyboard users
- [ ] `aria-live` regions for dynamic content updates
- [ ] No `tabindex` > 0 (disrupts natural tab order)

### 2. Focus States & Keyboard Navigation

- [ ] All interactive elements are focusable
- [ ] Focus indicator is visible (never `outline: none` without replacement)
- [ ] Tab order follows visual layout
- [ ] Modal/dialog traps focus within
- [ ] Escape key closes modals/popups
- [ ] Enter/Space activates buttons
- [ ] Arrow keys navigate within components (tabs, menus, grids)

### 3. Forms

- [ ] Labels visually associated with inputs
- [ ] Error messages are specific (not just "invalid")
- [ ] Required fields marked clearly
- [ ] Autocomplete attributes on common fields
- [ ] Input types match content (email, tel, url, number)
- [ ] Form validation happens on submit AND on blur
- [ ] Success/error states are clearly distinguishable

### 4. Animation & Motion

- [ ] `prefers-reduced-motion` media query respected
- [ ] No auto-playing animations that can't be paused
- [ ] No flashing content (< 3 flashes per second)
- [ ] Transition duration: 150–500ms (not too fast, not too slow)
- [ ] Animations use `transform` and `opacity` (GPU-accelerated)
- [ ] No layout-triggering animations (`width`, `height`, `top`, `left`)

### 5. Typography

- [ ] Base font size >= 16px on mobile (prevents iOS zoom)
- [ ] Line height 1.4–1.6 for body text
- [ ] Maximum line length: 60–80 characters
- [ ] Font loading: `font-display: swap` or `optional`
- [ ] Fallback fonts specified in font stack
- [ ] No justified text (causes uneven spacing)
- [ ] Heading hierarchy: only one `<h1>`, sequential levels

### 6. Images & Media

- [ ] Images have explicit `width` and `height` (prevents CLS)
- [ ] Responsive images with `srcset` or `<picture>`
- [ ] Lazy loading for below-the-fold images
- [ ] WebP/AVIF format with fallbacks
- [ ] SVG for icons and logos (not PNG)
- [ ] Video: controls provided, no autoplay with sound

### 7. Performance

- [ ] Critical CSS inlined or preloaded
- [ ] Non-critical CSS loaded asynchronously
- [ ] JavaScript deferred or async
- [ ] No render-blocking resources in `<head>`
- [ ] Fonts preloaded (`<link rel="preload">`)
- [ ] Minimal DOM depth (< 32 levels)
- [ ] No unused CSS/JS in bundle

### 8. Navigation & State

- [ ] Current page/section indicated in navigation
- [ ] Breadcrumbs for deep hierarchies
- [ ] Back button works correctly (browser history)
- [ ] URL reflects current state (deep-linking)
- [ ] 404 page is helpful (not just "not found")
- [ ] Loading states for all async operations
- [ ] Empty states for lists with no data

### 9. Dark Mode & Theming

- [ ] Dark mode: backgrounds layered (not just inverted)
- [ ] Dark mode: shadows adjusted (subtle, colored)
- [ ] Dark mode: images/icons have appropriate contrast
- [ ] CSS custom properties for theme values
- [ ] `prefers-color-scheme` media query supported
- [ ] Theme toggle persists across sessions

### 10. Touch & Mobile

- [ ] Touch targets >= 44x44px
- [ ] Adequate spacing between touch targets (>= 8px)
- [ ] No hover-only interactions on mobile
- [ ] Swipe gestures have button alternatives
- [ ] No fixed elements covering content on mobile
- [ ] Viewport meta tag prevents unwanted zoom

### 11. Locale & i18n

- [ ] Text direction support (LTR/RTL)
- [ ] Date/time formats localized
- [ ] Number formats localized (decimal separators)
- [ ] Currency symbols correctly placed
- [ ] UI accommodates text expansion (translations can be 30-50% longer)
- [ ] Korean typography: Noto Sans KR or Pretendard for body text

### 12. Responsive Design

- [ ] Mobile-first approach (min-width breakpoints)
- [ ] Breakpoints: 320px, 768px, 1024px, 1440px
- [ ] No horizontal scroll (except intentional carousels/tables)
- [ ] Images scale down properly
- [ ] Tables: horizontal scroll wrapper or responsive layout
- [ ] Navigation: hamburger menu on mobile with accessible toggle
- [ ] Font sizes adjust for screen size (clamp() or media queries)

## Quick Fix Patterns

### Bad: No focus indicator
```css
/* DON'T */
*:focus { outline: none; }

/* DO */
*:focus-visible { outline: 2px solid var(--blue); outline-offset: 2px; }
```

### Bad: Color-only error indication
```html
<!-- DON'T -->
<input style="border-color: red">

<!-- DO -->
<input style="border-color: red" aria-invalid="true" aria-describedby="error-msg">
<span id="error-msg" role="alert">This field is required</span>
```

### Bad: Non-responsive table
```css
/* DO: wrap tables for mobile */
.table-wrapper { overflow-x: auto; -webkit-overflow-scrolling: touch; }
```

### Bad: Inaccessible button
```html
<!-- DON'T -->
<div onclick="doThing()">Click me</div>

<!-- DO -->
<button type="button" onclick="doThing()">Click me</button>
```

## Scoring Guide

When auditing, rate each category 1–5:
- **5**: Excellent, exceeds standards
- **4**: Good, meets all requirements
- **3**: Acceptable, minor issues
- **2**: Below standard, needs work
- **1**: Critical issues, must fix

Priority: Fix all 1s and 2s first. Then improve 3s. 4s and 5s are polish.
