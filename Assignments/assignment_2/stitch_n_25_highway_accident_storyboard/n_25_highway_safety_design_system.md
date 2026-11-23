---
name: "N-25 Highway Safety — Design System"
description: "High-contrast dark editorial data-visualization design system for the Balochistan N-25 road safety story."
---

## Overview

The N-25 Highway Safety design system supports a six-screen editorial data-visualization story about road accidents on Balochistan's N-25 (Quetta to Karachi) highway, created for a university HCI and Computer Graphics assignment. The aesthetic is restrained, journalistic, and strictly functional: a deep charcoal canvas grounds off-white typography, a single amber warning accent highlights fatalities, hotspots, and primary actions, and a muted blue-gray carries secondary metrics and comparisons. Every chart is labeled directly without legends, free of 3D effects or decorative chrome, and engineered for WCAG AA contrast and immediate readability at 1440px desktop width.

## Colors

The palette uses a deep charcoal surface hierarchy paired with crisp off-white text, a single amber warning accent for key numbers and hazard hotspots, and a muted blue-gray for secondary data series and structural context.

- **Primary (Amber Warning):** Reserved exclusively for key statistics, high-severity route hotspots, primary call-to-action buttons, and active story progress.
- **Secondary (Muted Blue-Gray):** Used for comparative/secondary data series, inactive progress indicators, axis hairlines, and supporting metadata.
- **Surfaces:** Deep charcoal tiers (`surface`, `surface-container-low`, `surface-container`, `surface-container-high`) create subtle flat separation without drop shadows.

```yaml
colors:
  primary: "#FFB95F"
  on-primary: "#2A1700"
  primary-container: "#F59E0B"
  on-primary-container: "#1A0E00"
  secondary: "#9CADC3"
  on-secondary: "#0B1D2D"
  secondary-container: "#213243"
  on-secondary-container: "#D3E4FB"
  tertiary: "#7FD0FF"
  on-tertiary: "#001E2D"
  error: "#FFB4AB"
  on-error: "#410002"
  background: "#16181D"
  on-background: "#F0F0F7"
  surface: "#16181D"
  on-surface: "#F0F0F7"
  surface-container-lowest: "#101216"
  surface-container-low: "#1C1F26"
  surface-container: "#23262E"
  surface-container-high: "#2C303A"
  surface-container-highest: "#363B47"
  on-surface-variant: "#C6C9D4"
  outline: "#8192A7"
  outline-variant: "#323743"
  inverse-surface: "#F0F0F7"
  inverse-on-surface: "#16181D"
```

## Typography

**Inter** is used exclusively across all roles to maximize legibility in data-dense visualizations and editorial storytelling. Display numerals and tabular figures use `tabular-nums` (`tnum`) so aligned metrics never jitter. Screen titles are `56px` or larger, body copy is `18px` or larger, and all chart labels are `16px` or larger.

```yaml
typography:
  display-xl:
    fontFamily: "Inter"
    fontSize: 96px
    fontWeight: 700
    lineHeight: 104px
    letterSpacing: -2.5px
    fontFeature: "'tnum' 1"
  display-xl-mobile:
    fontFamily: "Inter"
    fontSize: 32px
    fontWeight: 700
    lineHeight: 38px
    letterSpacing: -0.5px
    fontFeature: "'tnum' 1"
  display-lg:
    fontFamily: "Inter"
    fontSize: 64px
    fontWeight: 700
    lineHeight: 72px
    letterSpacing: -1.5px
  display-lg-mobile:
    fontFamily: "Inter"
    fontSize: 32px
    fontWeight: 700
    lineHeight: 38px
    letterSpacing: -0.5px
  headline-lg:
    fontFamily: "Inter"
    fontSize: 56px
    fontWeight: 700
    lineHeight: 64px
    letterSpacing: -1.2px
  headline-lg-mobile:
    fontFamily: "Inter"
    fontSize: 30px
    fontWeight: 700
    lineHeight: 36px
    letterSpacing: -0.4px
  headline-md:
    fontFamily: "Inter"
    fontSize: 36px
    fontWeight: 600
    lineHeight: 44px
    letterSpacing: -0.6px
    fontFeature: "'tnum' 1"
  headline-md-mobile:
    fontFamily: "Inter"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 30px
    letterSpacing: -0.3px
    fontFeature: "'tnum' 1"
  title-lg:
    fontFamily: "Inter"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 32px
    letterSpacing: -0.2px
  body-lg:
    fontFamily: "Inter"
    fontSize: 20px
    fontWeight: 400
    lineHeight: 30px
    letterSpacing: 0px
  body-md:
    fontFamily: "Inter"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 28px
    letterSpacing: 0px
  label-lg:
    fontFamily: "Inter"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 22px
    letterSpacing: 0.1px
    fontFeature: "'tnum' 1"
  label-md:
    fontFamily: "Inter"
    fontSize: 16px
    fontWeight: 500
    lineHeight: 22px
    letterSpacing: 0.1px
    fontFeature: "'tnum' 1"
  label-sm:
    fontFamily: "Inter"
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
    letterSpacing: 0.2px
    fontFeature: "'tnum' 1"
```

## Layout & Spacing

Designed for a **1440px desktop** viewport using a **12-column fixed-max-width grid** (`1280px` max content width, `80px` horizontal page padding, `24px` column gutters) and an **8px base spacing scale**. Generous vertical and horizontal whitespace frames a single focal narrative per screen, with a consistent top navigation bar (story title + 6-step progress indicator) and a consistent bottom footer (`Source: [to be added]` + Previous / Next screen navigation).

```yaml
spacing:
  gutter-xs: 4px
  gutter-sm: 8px
  gutter-md: 16px
  gutter-lg: 24px
  gutter-xl: 32px
  section: 48px
  page-margin: 80px
```

## Elevation & Depth

Strictly flat, 2D editorial presentation. No drop shadows, no 3D extrusions, no glassmorphism, and no glowing blurs. Hierarchy is established solely through tonal surface steps (`surface` -> `surface-container-low` -> `surface-container`) and hairline `1px` `outline-variant` borders.

## Shapes

Clean, architectural geometry with modest corner rounding for cards and buttons, and full pills for progress dots and route markers.

```yaml
rounded:
  sm: 4px
  DEFAULT: 8px
  md: 12px
  lg: 16px
  full: 9999px
```

## Motion & Micro-interaction

Subtle, crisp transitions on interactive navigation controls (`150ms ease-out`). Data visualizations render statically and clearly with zero distracting loops or decorative animation.

```yaml
motion:
  state-change:
    duration: 150ms
    delay: 0ms
    timingFunction: ease-out
  surface-enter:
    duration: 250ms
    delay: 0ms
    timingFunction: cubic-bezier(0.2, 0, 0, 1)
```

## Voice & Content Strategy

- **Tone:** Factual, journalistic, urgent yet restrained.
- **Data Integrity:** Never invent statistics. Use `[XX]` placeholders or numbers explicitly labeled `SAMPLE DATA`. Every screen includes `Source: [to be added]` in the footer.
- **Accessibility:** Never rely on color alone to convey meaning; pair amber/blue-gray distinctions with direct text labels, percentages, and explicit status tags.

## Components

Component implementations live as individual HTML sticker sheet files in
`components/`. Each file contains the canonical, styled HTML components with
`<!-- COMPONENT: name -->` comment markers. Read each file before use.

- **Button** → `@components/button.html`: `button-primary`, `button-icon`, `button-with-icon`
- **Card** → `@components/card.html`: `card-elevated`, `card-action`, `card-interactive`, `card-interactive-2`
- **Typography** → `@components/typography.html`: `typography-display`, `typography-body`, `typography-label`
