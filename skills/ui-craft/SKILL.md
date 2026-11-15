---
name: ui-craft
description: "Apply grounded UI, typography, color, spacing, and media performance rules. Use when designing, building, or reviewing web interfaces and CSS so they look deliberately engineered rather than AI-generated."
---

# ui-craft

Left unconstrained, code models converge on the same visual defaults: multi-color `radial-gradient` background blobs, pitch-black dark mode, oversized `24px+` rounded cards that bounce and zoom on hover, and bold headings everywhere. This skill replaces those defaults with a disciplined design system grounded in the 3P framework (*Purpose, Principles, Personality*).

## 1. The 60-30-10 Color Rule & Cohesive Neutrals

Every interface follows a strict color budget:

- **60% Canvas & Primary Surfaces:** Matte neutral backgrounds. Never layer multi-color `radial-gradient` aurora blobs (purple, cyan, pink, peach) onto `body` or card backgrounds.
- **30% Cards & Structural UI:** Elevated surfaces, trays, and subtle `1px` borders.
- **10% Accent / CTA:** Reserved exclusively for primary actions, active indicators, and focus states. Never assign five different neon accent colors to adjacent cards.
- **Harmonious OKLCH / Tinted Neutrals:** Lock backgrounds, surfaces, text, and borders to a consistent hue angle (for example `265°` cool slate) with low chroma (`0.01` to `0.04`).
- **Soft Dark Mode (`22%` to `24%` lightness):** Avoid harsh `#000000` contrast. Use a soft midnight slate (`oklch(23% 0.022 265)` / `#181d27`) with elevated cards (`#1e2636`) and a desaturated accent in dark mode so nothing vibrates against dark surfaces.

## 2. Fluid Typography, Hierarchy & Measure

- **Maximum 2 Font Families:** Pair one display/heading typeface with one high-legibility body typeface (plus a monospace face for code/metadata).
- **Fluid Type Scale (`clamp`):** Scale smoothly from a `1.2` modular ratio on mobile to desktop without abrupt breakpoint jumps:
  - Display: `clamp(2.25rem, 4vw + 1.25rem, 4rem)`
  - H1: `clamp(1.875rem, 3vw + 1rem, 3rem)`
  - H2: `clamp(1.5rem, 1.5vw + 1.1rem, 2.25rem)`
  - H3: `clamp(1.25rem, 1vw + 0.95rem, 1.65rem)`
  - Body: `1rem` (`16px`)
- **Weight, Leading & Tracking:**
  - Let size carry the hierarchy on large headings (`400` or `500` weight with tight line-height `1.12` to `1.2` and negative letter-spacing `-0.02em` to `-0.03em`) instead of defaulting to `font-bold` on every heading.
  - Set body copy to `line-height: 1.5` to `1.6` and cap paragraph width at `max-width: 62ch`.

## 3. 8pt Spacing Grid, Restrained Radii & Calm Motion

- **8pt Spacing System:** Use `4px | 8px | 16px | 24px | 32px | 48px | 64px | 96px` with fluid section padding `clamp(4rem, 8vw, 7.5rem)`. Keep spacing tight within related groups and generous between sections.
- **Tactile Radii (`6px` to `14px`):** Use `6px` for small badges/buttons, `8px` to `12px` for inputs and inner cards, and `12px` to `14px` for showcase containers. Avoid bloated `24px+` bubble cards.
- **Subtle Depth & Calm Hover:** Use a crisp `1px` low-opacity border and restrained shadow (`0 8px 24px -12px rgba(0, 0, 0, 0.12)`). Keep imagery still on hover (no `hover:scale-105` or card bounce); signal hover with a subtle border transition.
- **Clear Input Affordance:** Keep free-text inputs visually distinct from suggestion chips with a static, open placeholder.

## 4. Viewport-Aware Media & Asset Performance

- Serve video in `.webm` first with `.mp4` as fallback, and pause `<video>` elements automatically when scrolled out of the viewport (`IntersectionObserver` or `ScrollTrigger`).
- Never lazy-load above-the-fold hero media (`loading="eager"` or `<link rel="preload">`). Always set `loading="lazy"` and `decoding="async"` on below-the-fold imagery.
