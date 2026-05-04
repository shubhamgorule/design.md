---
version: alpha
name: Product Designer Portfolio
description: Minimal warm-dark canvas, Source Serif 4 + DM Sans. Orange appears only on the primary call-to-action.
colors:
  primary: "#f4f1ea"
  secondary: "#9c958c"
  tertiary: "#f97316"
  tertiary-dim: "#ea580c"
  neutral: "#110e0c"
  surface: "#1c1714"
  on-surface: "#f4f1ea"
  on-surface-variant: "#b5aea5"
  outline: "#3f342c"
  on-tertiary: "#100d0b"
  tertiary-container: "#2d1810"
  on-tertiary-container: "#fdba74"
typography:
  headline-display:
    fontFamily: "Source Serif 4"
    fontSize: 3.2rem
    fontWeight: 600
    lineHeight: 1.12
    letterSpacing: -0.012em
  headline-lg:
    fontFamily: "Source Serif 4"
    fontSize: 2.125rem
    fontWeight: 600
    lineHeight: 1.18
    letterSpacing: -0.01em
  headline-md:
    fontFamily: "Source Serif 4"
    fontSize: 1.375rem
    fontWeight: 600
    lineHeight: 1.32
    letterSpacing: -0.008em
  body-lg:
    fontFamily: "DM Sans"
    fontSize: 1.125rem
    fontWeight: 400
    lineHeight: 1.68
  body-md:
    fontFamily: "DM Sans"
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.62
  body-sm:
    fontFamily: "DM Sans"
    fontSize: 0.875rem
    fontWeight: 400
    lineHeight: 1.55
  label-md:
    fontFamily: "DM Sans"
    fontSize: 0.75rem
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.1em
rounded:
  sm: 4px
  md: 6px
  lg: 10px
  xl: 14px
  full: 9999px
spacing:
  xs: 8px
  sm: 16px
  md: 24px
  lg: 48px
  xl: 72px
  gutter: 28px
  section: 112px
components:
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 14px 22px
    height: 48px
  button-primary-hover:
    backgroundColor: "{colors.tertiary-dim}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 0
  button-secondary-hover:
    backgroundColor: "transparent"
  card-project:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
  nav-link:
    typography: "{typography.body-sm}"
    textColor: "{colors.secondary}"
  tag-chip:
    backgroundColor: "{colors.tertiary-container}"
    textColor: "{colors.on-tertiary-container}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.sm}"
    padding: 4px 0
---

## Overview

**Minimal first:** warm near-black ground, cream type, hairline dividers. **Source Serif 4** carries headlines—upright, book-drawn strokes with lining figures; it reads **human but disciplined** next to **DM Sans** for body, labels, and buttons. **Orange is intentionally scarce:** reserved for the **solid primary button** (and its hover darken). Links, nav hovers, eyebrows, timeline, and card hovers stay in **primary / secondary / outline** so the layout feels quiet until someone hits the main action.

## Colors

**Near-black warm ground** with **orange only where conversion matters.**

- **Primary (#F4F1EA):** Main text, nav hover, emphasis.
- **Secondary (#9C958C):** Nav at rest, eyebrows, de-emphasized lines.
- **Tertiary (#F97316):** **`button-primary` fill only** in the default implementation.
- **Tertiary dim (#EA580C):** `button-primary-hover` background.
- **On-tertiary (#100D0B):** Label on solid orange buttons (contrast-safe).
- **Neutral / surface / outline:** Structure without hue noise.
- **Tertiary container / on-container:** Optional muted chips—omit if unused.

## Typography

**Source Serif 4** at **600** for **display and section titles**—news-grade serif, vertical stress, no “wobbly” display personality. Enable **lining figures** where supported. **DM Sans** for **body, UI labels (uppercase tracking), and buttons** so long copy and chrome stay clear next to serif headlines.

## Layout

Centered column ~**1040px**, generous section padding. **No orange washes** on the page background.

## Elevation & Depth

**Work cards:** no border on the tile; image on top, copy below. Hover adds a **neutral grain / light mesh** on the thumbnail (no orange in the texture). Typography steps from **secondary** toward **primary** on hover.

## Shapes

Slight rounding (**6–10px**) on thumbnails and buttons; timeline markers use **outline** neutrals, not orange fills.

## Components

- **Primary button:** solid **tertiary**, **on-tertiary** text—**the default home for orange**.
- **Ghost / text CTA:** cream / white hover; underline uses **outline** or **primary**, not orange.
- **Nav:** hover → **primary**; no pill chrome.
- **Project cards:** as above—orange does not appear on cards unless you deliberately add a campaign badge.

## Do's and Don'ts

- Do treat orange as **one alarm bell**—when users see it, they should know it’s the **main action**.
- Do let **type and spacing** carry personality; do not compensate with more orange.
- Don’t tint every divider, eyebrow, link, or focus ring orange—use **cream** focus where possible.
- Don’t drop below **4.5:1** for body text; keep **dark** labels on orange buttons.
