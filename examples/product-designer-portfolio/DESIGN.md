---
version: alpha
name: Product Designer Portfolio
description: Editorial, case-study-first portfolio surface for a senior product designer.
colors:
  primary: "#0f172a"
  secondary: "#64748b"
  tertiary: "#2563eb"
  neutral: "#f8fafc"
  surface: "#ffffff"
  on-surface: "#0f172a"
  on-surface-variant: "#475569"
  outline: "#e2e8f0"
  tertiary-container: "#dbeafe"
  on-tertiary-container: "#1e3a8a"
typography:
  headline-display:
    fontFamily: "Fraunces"
    fontSize: 3.5rem
    fontWeight: 600
    lineHeight: 1.05
    letterSpacing: -0.03em
  headline-lg:
    fontFamily: "Fraunces"
    fontSize: 2.25rem
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -0.02em
  headline-md:
    fontFamily: "Fraunces"
    fontSize: 1.5rem
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: -0.01em
  body-lg:
    fontFamily: "DM Sans"
    fontSize: 1.125rem
    fontWeight: 400
    lineHeight: 1.65
  body-md:
    fontFamily: "DM Sans"
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "DM Sans"
    fontSize: 0.875rem
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: "DM Sans"
    fontSize: 0.75rem
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.12em
rounded:
  sm: 6px
  md: 10px
  lg: 16px
  xl: 24px
  full: 9999px
spacing:
  xs: 8px
  sm: 16px
  md: 24px
  lg: 40px
  xl: 64px
  gutter: 24px
  section: 96px
components:
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "#ffffff"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 14px 22px
    height: 48px
  button-primary-hover:
    backgroundColor: "#1d4ed8"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: 14px 22px
    height: 48px
  button-secondary-hover:
    backgroundColor: "{colors.neutral}"
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
    padding: 8px 14px
---

## Overview

This portfolio reads as **confident editorial craft**: generous whitespace, a single serif display voice for headlines, and a restrained sans for narrative and metadata. The personality is clear and senior—built for recruiters and hiring managers scanning case studies, not decorative chrome.

The emotional response should feel **calm, precise, and trustworthy**, like a well-typeset annual report or design journal. Motion (if added later) stays subtle; hierarchy comes from scale, weight, and spacing—not from loud color blocks.

## Colors

The palette is anchored in **slate ink** on **cool paper**, with **one saturated blue** reserved for primary actions and key links.

- **Primary (#0F172A):** Headlines, body text, and navigation emphasis. Maximum readability on light surfaces.
- **Secondary (#64748B):** Supporting copy, captions, and inactive nav—keeps density readable without competing with work imagery.
- **Tertiary (#2563EB):** The single interaction accent—primary buttons, inline links, and focus rings.
- **Neutral (#F8FAFC):** Page canvas and alternating section bands to separate story blocks.
- **Surface (#FFFFFF):** Cards and project tiles for a crisp lift from the neutral field.

## Typography

**Fraunces** carries display and section titles—soft contrast and optical sizing suit portfolio hero lines. **DM Sans** handles everything else: bios, case study blurbs, labels, and UI chrome.

- **Display / headlines:** Fraunces semibold, tight negative tracking for impact at large sizes.
- **Body:** DM Sans regular at 16–18px for long-form case summaries.
- **Labels:** DM Sans semibold, uppercase tracking for roles, dates, and section kicker lines.

## Layout

Layout follows a **centered column** with a **max readable width of 1120px** and **24px gutters** on smaller viewports.

- **Vertical rhythm:** Major sections use 96px top/bottom padding; within sections, stack related groups with 40px gaps.
- **Case study grid:** On wide screens, featured work uses a two-column grid with 24px gutters; cards share equal visual weight so thumbnails do the talking.

## Elevation & Depth

The surface is intentionally **flat**. Depth is communicated with:

- **1px hairline borders** (`outline` token) on cards instead of heavy shadows.
- **Optional shadow** on hero or primary CTA only: a single soft `0 24px 48px rgba(15, 23, 42, 0.08)` for the first fold—never stacked on every card.

## Shapes

Corners are **moderately rounded** (10–16px) to feel contemporary without toy-like pill aesthetics. Chips and tags use full rounding; imagery inside cards stays rectangular with `16px` outer radius on the container only.

## Components

### Navigation

Top bar is minimal: wordmark left, text links right. Active section uses `tertiary` underline or weight shift—not a filled pill.

### Project cards

White surface, hairline border, padding 24px. Title in `headline-md`, meta line in `body-sm` + `secondary`. Optional tag row uses `tag-chip` tokens.

### Buttons

Primary actions use `button-primary`; secondary outline-style uses `button-secondary` with visible border implied in implementation (token uses transparent fill; border is described in prose for consumers).

### Tags

Small uppercase labels for **Product**, **Systems**, **Research**—always `tertiary-container` fill so they read as taxonomy, not decoration.

## Do's and Don'ts

- Do let case study imagery and typography carry the page; avoid more than one accent color in a single viewport.
- Do maintain WCAG AA contrast for all text on `surface` and `neutral` (4.5:1 minimum).
- Don't use Fraunces below 18px for body copy—switch to DM Sans for legibility.
- Don't mix more than two font weights in a single component (e.g., card title + excerpt).
