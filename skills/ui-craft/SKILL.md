---
name: ui-craft
description: "Apply grounded UI, typography, color, spacing, and media performance rules. Use when designing, building, or reviewing web interfaces and CSS so they look deliberately engineered rather than AI-generated."
---

# ui-craft

Left unconstrained, code models converge on the same visual defaults: multi-color `radial-gradient` background blobs, pitch-black dark mode, oversized `24px+` rounded cards that bounce on hover, floating glassmorphism pills, and bold headings everywhere. This skill replaces those defaults with a disciplined design system grounded in **Matt D. Smith's (MDS / [Shift Nudge](https://shiftnudge.com)) 3P framework (*Purpose, Principles, Personality*)**:

1. **Purpose (*What is this for?*):** Every screen and element must solve a concrete user task and earn its place before high-fidelity styling begins.
2. **Principles (*How is it structured?*):** Non-negotiable standards for color harmony, fluid typography, spacing, contrast (WCAG 2.1 AA), and responsiveness.
3. **Personality (*What does it feel like?*):** Brand voice, surface materiality, corner radii, and motion layered on top of a functional foundation (Aarron Walter's hierarchy of user needs in *Designing for Emotion*: *Functional → Reliable → Usable → Delightful*).

## 1. Gallery Principle, Color Budget & Curated Light Rhythm

Every interface follows a strict color budget so the product or content carries the color rather than the surrounding chrome:

- **Gallery Principle (Achromatic Chrome + White Product Grounds):** On editorial, marketing, and portfolio sites, keep UI chrome strictly achromatic (`#ffffff` pure surfaces, `#f7f7f7` alabaster canvas, `#1a1a1a` primary ink, `#575757` body copy, `#8a8a8a` metadata, `rgba(26, 26, 26, 0.11)` hairline borders) with zero colored UI accents. Stage product screenshots, mockups, and videos on crisp `#ffffff` grounds rather than dark card walls so each product's own palette stands apart. Never layer `radial-gradient` aurora blobs onto `body` or card backgrounds.
- **Curated Light Rhythm Over Theme Toggles:** For editorial, marketing, and portfolio sites, ship one fully art-directed light experience punctuated by 1 to 2 intentional full-bleed dark contrast bands (`#1a1a1a` next-step footer bands or data callouts) to rest the eye instead of maintaining a dual light/dark toggle that compromises image staging.
- **60-30-10 Budget & Optional App Dark Mode:** For daily-use applications that require brand accents or dark mode, follow 60% matte neutral canvas, 30% structural surfaces, and 10% single accent, using soft dark-mode lightness (`22%` to `24%`, such as `oklch(23% 0.022 265)` / `#181d27`) rather than `#000000`.

## 2. Fluid Typography, Light Display Hierarchy & Editorial Rhythm

- **Maximum 2 Font Families:** Pair one display/heading typeface with one high-legibility body typeface (plus a monospace face for code and uppercase metadata labels).
- **Fluid Type Scale (`clamp`, via [Utopia.fyi](https://utopia.fyi)):** Scale smoothly from mobile to desktop without abrupt breakpoint jumps:
  - Display: `clamp(2.25rem, 4vw + 1rem, 3.75rem)`
  - H1: `clamp(1.875rem, 3vw + 1rem, 3.25rem)`
  - H2: `clamp(1.5rem, 1.5vw + 1.1rem, 2.25rem)`
  - H3: `clamp(1.25rem, 1vw + 0.95rem, 1.5rem)`
  - Body: `1rem` (`16px` to `17px`)
- **Weight, Leading & Editorial Contrast:**
  - Let scale and whitespace carry hierarchy on large headings (`300` light or `400` regular weight, tight line-height `1.06` to `1.15`, negative letter-spacing `-0.02em` to `-0.03em`) instead of defaulting to `font-bold`.
  - Set body copy to `line-height: 1.55` to `1.7` and cap prose width at `max-width: 62ch`, letting showcase media break wider (`max-width: 64rem` or full bleed) to create gallery rhythm.

## 3. 8pt Spacing Grid, Architectural Geometry & Zero-Latency Motion

- **8pt Spacing System:** Use `4px | 8px | 16px | 24px | 32px | 48px | 64px | 96px` with generous section padding (`clamp(4.5rem, 8vw, 7.5rem)`) and wide card gutters so layouts breathe.
- **Architectural Radii (`2px` to `6px`) & Flat Surface Contrast:** Default to crisp `2px` to `6px` radii on media stages, cards, and buttons (`0` drop-shadow on cards; separate `#ffffff` surfaces from `#f7f7f7` ground with `1px` low-opacity borders `rgba(26, 26, 26, 0.06)` to `0.11`). Avoid `14px+` shadowed bubble cards.
- **Flat Visible Top Navigation:** Use a clean, flat sticky top bar (`bg-white/92`, `1px` bottom border) with all 3 to 6 top-level links visible on desktop and underlined when active. Never hide short desktop menus behind a hamburger button, never use floating glassmorphism pills, and omit redundant brand/author names in the navbar when the hero already states them.
- **Zero Blocking Motion or Scroll Hijacking:** Never hijack native scroll (virtual scroll), block route changes with page-transition overlays, use custom cursors, or gate content behind intro prologues. Keep feedback instantaneous (`150ms` to `200ms` border/color transitions and subtle `1.02` media scale inside overflow-clipped frames, disabled under `prefers-reduced-motion`).
- **Clear Input Affordance & `?` Tooltips:** Keep free-text inputs visually distinct from suggestion chips with a static placeholder. Keep headings free of explanatory parentheticals, moving optional clarifications into a compact `?` tooltip button that works on hover, focus, and tap.

## 4. Viewport-Aware Media & Asset Performance

- Serve video in `.webm` first with `.mp4` as fallback, and pause `<video>` elements automatically when scrolled out of the viewport (`IntersectionObserver` or `ScrollTrigger`).
- Never lazy-load above-the-fold hero media (`loading="eager"` or `<link rel="preload">`). Always set `loading="lazy"` and `decoding="async"` on below-the-fold imagery.
