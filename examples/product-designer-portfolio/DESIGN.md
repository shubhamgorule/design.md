---
version: alpha
name: Product Designer Portfolio
description: Dark, minimal portfolio surface—bold type, near-monochrome, one structural accent.
colors:
  primary: "#fafafa"
  secondary: "#737373"
  tertiary: "#fafafa"
  neutral: "#09090b"
  surface: "#0f0f10"
  on-surface: "#fafafa"
  on-surface-variant: "#a3a3a3"
  outline: "#262626"
  tertiary-container: "#171717"
  on-tertiary-container: "#e5e5e5"
typography:
  headline-display:
    fontFamily: "Space Grotesk"
    fontSize: 4rem
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: -0.04em
  headline-lg:
    fontFamily: "Space Grotesk"
    fontSize: 2.5rem
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.03em
  headline-md:
    fontFamily: "Space Grotesk"
    fontSize: 1.375rem
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.02em
  body-lg:
    fontFamily: Inter
    fontSize: 1.125rem
    fontWeight: 400
    lineHeight: 1.65
  body-md:
    fontFamily: Inter
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Inter
    fontSize: 0.875rem
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: Inter
    fontSize: 0.6875rem
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.14em
rounded:
  sm: 2px
  md: 4px
  lg: 8px
  xl: 12px
  full: 9999px
spacing:
  xs: 8px
  sm: 16px
  md: 24px
  lg: 40px
  xl: 64px
  gutter: 24px
  section: 104px
components:
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.neutral}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 16px 24px
    height: 52px
  button-primary-hover:
    backgroundColor: "#e5e5e5"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 16px 24px
    height: 52px
  button-secondary-hover:
    backgroundColor: "{colors.surface}"
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
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 8px 12px
---

## Overview

This portfolio is **dark, minimal, and loud through typography alone**. Almost everything sits on near-black with **one high-contrast axis**: huge geometric headlines in Space Grotesk, quiet Inter for supporting copy, and **white-on-ink** for the primary action. Decorative color is avoided; rhythm and weight carry the brand.

The feeling is **editorial and direct**—gallery wall, not dashboard. Motion stays optional; when used, it should be fast and sparse (opacity or 4–8px translate), never bouncy.

## Colors

The system is **monochrome-first**. Surfaces are stepped blacks and charcoals; text is off-white for reduced glare. Borders are single-pixel zinc hairlines—visible but quiet.

- **Primary (#FAFAFA):** Headlines, wordmark, and primary button label pair (with dark fill context in implementation).
- **Secondary (#737373):** Navigation at rest, captions, metadata.
- **Tertiary (#FAFAFA):** Reserved for **solid fills** that must read as “the” action (e.g. primary button background)—same chroma as primary, different role.
- **Neutral (#09090B):** Global page canvas.
- **Surface (#0F0F10):** Cards, hero aside, and alternating bands—one step above canvas.
- **Outline (#262626):** Dividers and card strokes only—no drop shadows in the default spec.

## Typography

**Space Grotesk** at **700** owns display and section titles—tight tracking, large sizes, minimal line height for impact. **Inter** handles body, excerpts, and UI labels at **400/600** only.

- **Display:** Space Grotesk Bold, up to ~4rem desktop; never smaller than ~2.25rem for the main hero line on mobile.
- **Body:** Inter Regular 16–18px; max line length ~60 characters where possible.
- **Labels:** Inter Semibold, uppercase, wide tracking—used for section kickers and tags.

## Layout

A **single centered column** (max **1120px**) with **24px gutters**. Sections breathe: **~104px** vertical padding. The work grid is **two columns** on large screens with a **24px** gutter; stacks to one column on narrow viewports.

## Elevation & Depth

**No elevation by default.** Hierarchy is **type scale + surface step + outline**. If a consumer adds shadow for marketing hero only, use a single **soft, large diffuse** (e.g. `0 32px 64px rgba(0,0,0,0.45)`)—never on every card.

## Shapes

**Sharp minimal:** default corners are **2–8px**—barely rounded, engineered, not playful. Tags keep **pill** (`full`) as the only strongly rounded elements.

## Components

### Navigation

Fixed or sticky top bar: **transparent-to-canvas** blur optional. Links use `nav-link`; hover moves to **primary** text color, no background pill.

### Project cards

`card-project` token: **surface** fill, **outline** border, **24px** padding. Thumbnails sit in a muted inner frame (dark gradient or real imagery). Hover may lighten **outline** by one step only—no colored glow.

### Buttons

**Primary:** white (`tertiary`) fill, **neutral** (#09090B) label for maximum contrast. **Secondary:** transparent, **outline** border, **primary** text.

### Tags

Use `tag-chip`: **tertiary-container** background, **on-tertiary-container** text—low contrast chips that read as taxonomy.

## Do's and Don'ts

- Do keep the canvas consistently **neutral**; reserve **surface** for contained content only.
- Do verify **4.5:1** contrast for all body text on **surface** and **neutral**.
- Don't introduce a second accent hue in the default theme—breaks the minimal contract.
- Don't use Space Grotesk below **18px** for paragraph text; switch to Inter.
