---
name: "University of Balochistan Design System"
description: "Calm, trustworthy, WCAG 2.2 AA accessible design system for the University of Balochistan, Quetta, built on deep academic green, warm gold, off-white surfaces, and Inter typography."
---

## Overview

The University of Balochistan design system embodies academic authority, regional heritage, and inclusive accessibility. Designed for prospective students, current scholars, faculty, and families across Balochistan and Pakistan, the interface prioritizes clarity, calm reading rhythm, generous whitespace, and strict WCAG 2.2 AA compliance.

The aesthetic pairs **Corporate / Modern** structural clarity with **Minimalism**'s breathing room: crisp 8px-grid alignment, 8px rounded corners, high-contrast typography in **Inter**, and a grounded palette of deep academic green, warm gold, and calm off-white.

## Colors

Deep academic green (`primary`) anchors institutional identity, primary navigation, and key headings. Warm gold (`accent`) is reserved for the primary "Apply Now" call to action and subtle academic highlights, always paired with dark ink (`on-accent`) to exceed 4.5:1 contrast. Off-white (`surface`) and pure white (`surface-container-lowest`) cards keep long-form reading effortless, paired with dark gray (`on-surface`) text.

- **Never rely on color alone:** Active navigation items combine bold weight and a bottom underline; form states and alerts pair color with icons and explicit text labels.
- **Visible focus:** Every interactive element uses a high-contrast 3px focus ring (`primary` or `accent` depending on surface) with a 2px offset.

```yaml
colors:
  primary: "#144D32"
  on-primary: "#FFFFFF"
  primary-hover: "#00351F"
  primary-container: "#E3EAE3"
  on-primary-container: "#002111"
  accent: "#E5B238"
  on-accent: "#161D19"
  accent-hover: "#D4A024"
  secondary: "#7A5900"
  on-secondary: "#FFFFFF"
  secondary-container: "#FFEFD5"
  on-secondary-container: "#261900"
  surface: "#F7F9F7"
  on-surface: "#161D19"
  surface-container-lowest: "#FFFFFF"
  surface-container-low: "#EFF3EF"
  surface-container: "#E9EEE9"
  surface-container-high: "#E1E7E1"
  on-surface-variant: "#3D4540"
  outline: "#68706A"
  outline-variant: "#C4CCC5"
  error: "#BA1A1A"
  on-error: "#FFFFFF"
  error-container: "#FFDAD6"
  on-error-container: "#410002"
  success: "#144D32"
  on-success: "#FFFFFF"
```

## Typography

**Inter** is used across all display, headline, body, and label roles for crisp legibility at every size, including numeric tabular figures for dates, fees, and campus statistics. Body copy is set at a minimum of `16px` (`body-md`) with a `1.625` line height (`26px`) to ensure comfortable reading and 200% zoom resilience.

```yaml
typography:
  display-lg:
    fontFamily: "Inter"
    fontSize: 48px
    fontWeight: 700
    lineHeight: 56px
    letterSpacing: -0.5px
  display-lg-mobile:
    fontFamily: "Inter"
    fontSize: 32px
    fontWeight: 700
    lineHeight: 40px
    letterSpacing: -0.25px
  headline-lg:
    fontFamily: "Inter"
    fontSize: 36px
    fontWeight: 700
    lineHeight: 44px
    letterSpacing: -0.25px
  headline-lg-mobile:
    fontFamily: "Inter"
    fontSize: 28px
    fontWeight: 700
    lineHeight: 36px
    letterSpacing: -0.2px
  headline-md:
    fontFamily: "Inter"
    fontSize: 28px
    fontWeight: 600
    lineHeight: 36px
    letterSpacing: -0.15px
  headline-sm:
    fontFamily: "Inter"
    fontSize: 22px
    fontWeight: 600
    lineHeight: 30px
    letterSpacing: 0px
  title-lg:
    fontFamily: "Inter"
    fontSize: 20px
    fontWeight: 600
    lineHeight: 28px
    letterSpacing: 0px
  title-md:
    fontFamily: "Inter"
    fontSize: 18px
    fontWeight: 600
    lineHeight: 26px
    letterSpacing: 0px
  body-lg:
    fontFamily: "Inter"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 29px
    letterSpacing: 0px
  body-md:
    fontFamily: "Inter"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 26px
    letterSpacing: 0px
  label-lg:
    fontFamily: "Inter"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 24px
    letterSpacing: 0px
  label-md:
    fontFamily: "Inter"
    fontSize: 14px
    fontWeight: 600
    lineHeight: 20px
    letterSpacing: 0.1px
```

## Layout & Spacing

The desktop layout targets a `1440px` viewport with a centered `1280px` max-width content container and `80px` horizontal safe margins (`px-20` on 1440px, `px-6` on smaller viewports). All spacing strictly follows an **8px spacing grid** (`8px`, `16px`, `24px`, `32px`, `48px`, `64px`, `80px`). All interactive touch targets (buttons, nav links, utility controls, form inputs) maintain a minimum height of `44px`.

```yaml
spacing:
  gutter-xs: 8px
  gutter-sm: 16px
  gutter-md: 24px
  gutter-lg: 32px
  gutter-xl: 48px
  section: 64px
  page-margin: 80px
```

## Elevation & Depth

Hierarchy is established primarily through **tonal layers** (`surface` off-white canvas with `surface-container-lowest` pure white cards) and crisp `1px` `outline-variant` borders rather than heavy drop shadows. Subtle ambient elevation is used only on sticky navigation bars or hover states to preserve a calm, print-inspired academic clarity.

## Shapes

A consistent **8px** (`DEFAULT: 8px`) corner radius defines all cards, buttons, form inputs, callout panels, and framed photographs, creating a unified, approachable, and structured geometric language.

```yaml
rounded:
  sm: 4px
  DEFAULT: 8px
  md: 8px
  lg: 8px
  full: 9999px
```

## Motion & Micro-interaction

Motion is restrained, functional, and respects `prefers-reduced-motion`. Interactive state changes (button hover, link underline, focus ring) resolve in `150ms`. No auto-playing carousels, looping animations, or decorative motion are permitted.

```yaml
motion:
  state-change:
    duration: 150ms
    delay: 0ms
    timingFunction: ease-out
  surface-enter:
    duration: 200ms
    delay: 0ms
    timingFunction: cubic-bezier(0.2, 0, 0, 1)
```

## Voice & Content Strategy

- **Tone of voice:** Welcoming, authoritative, and plain-spoken. Avoids marketing buzzwords in favor of clear, factual academic guidance (e.g., "Explore BS and MPhil Programs" rather than "Reimagine Your Future").
- **Capitalisation:** Title Case for navigation, headings, and primary buttons; sentence case for body copy, descriptions, and form labels.
- **Iconography:** Icons are never used alone; every icon is paired with a visible text label and marked `aria-hidden="true"` when redundant.
- **Action labels:** Use clear verb phrases (`Apply Now`, `Browse Departments`, `Download Prospectus`, `Send Message`).

## Components

Component implementations live as individual HTML sticker sheet files in
`components/`. Each file contains the canonical, styled HTML components with
`<!-- COMPONENT: name -->` comment markers. Read each file before use.

- **Button** → `@components/button.html`: `button-primary`, `button-icon`, `button-with-icon`
- **Card** → `@components/card.html`: `card-elevated`, `card-action`, `card-interactive`, `card-interactive-2`
- **Input Field** → `@components/input-field.html`: `input-field-text`, `input-field-icon`
- **Table** → `@components/table.html`: `table-standard`, `table-interactive`, `table-selectable`
