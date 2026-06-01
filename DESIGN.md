# Zen Pensions LP Design System

## Overview

This landing page uses a calm financial product style: light backgrounds, dark green hierarchy, soft borders, rounded forms and restrained accent colors.

## Colors

| Token | Value | Usage |
| --- | --- | --- |
| `--white` | `#ffffff` | Cards, header and form fields |
| `--almost-white` | `#f8faf7` | Main page background |
| `--harp` | `#ebf0e9` | Soft green panels |
| `--cyan-mist` | `#ebfefe` | Light support surface |
| `--zen-green` | `#1c3e3f` | Main headings, buttons and dark panels |
| `--zen-green-dark` | `#142d2e` | Button hover |
| `--body-blue` | `#3f5372` | Paragraph text |
| `--light-blue` | `#8c98aa` | Input placeholders |
| `--grey-nickel` | `#bec6bb` | Borders |
| `--pink` | `#fd5e7d` | Eyebrows and small emphasis |
| `--yellow` | `#ffb100` | Accent on dark green sections |
| `--line-soft` | `rgba(28, 62, 63, 0.16)` | Header and footer dividers |

## Typography

### Fonts

- Headings, buttons and labels: `Sora`
- Body text: `NotoSans`
- Local files:
  - `assets/fonts/sora-variable.woff2`
  - `assets/fonts/noto-sans-variable.woff2`

### Scale

| Element | Size | Weight | Notes |
| --- | --- | --- | --- |
| H1 | `clamp(2.4rem, 4.8vw, 4.5rem)` | `620` default | Uses split title weights |
| H2 | `clamp(1.85rem, 3.6vw, 3.2rem)` | `620` default | Uses split title weights |
| H3 | `clamp(1.1rem, 1.6vw, 1.45rem)` | `620` | Card titles |
| Body | `16px` | `400` | Base page text |
| Eyebrow | `0.9rem` | `650` | Pink or yellow label |
| Form label | `0.85rem` | `700` | Dark green |

## Title Treatment

Main section titles are split into strong and light lines.

```html
<h2 class="split-title">
  <span class="title-strong">Strong title line</span>
  <span class="title-light">Light title line.</span>
</h2>
```

```css
.title-strong {
  font-weight: 780;
}

.title-light {
  font-weight: 360;
}
```

## Layout

| Token | Value | Usage |
| --- | --- | --- |
| `--section-max` | `86rem` | Maximum page content width |
| `--section-gap` | `clamp(4rem, 6vw, 5.5rem)` | Vertical section spacing |
| Section side padding | `clamp(1.25rem, 4vw, 2rem)` | Page gutter |
| Hero gap | `clamp(2rem, 4vw, 3.5rem)` | Gap between hero copy and form |

## Radius

| Token | Value | Usage |
| --- | --- | --- |
| `--radius-xl` | `3rem` | Large panels |
| `--radius-lg` | `2rem` | Cards |
| `--radius-pill` | `999px` | Buttons and inputs |
| Lead card | `2.2rem` | Form container |

## Shadows

| Token | Value | Usage |
| --- | --- | --- |
| `--shadow-soft` | `0 26px 80px rgba(28, 62, 63, 0.14)` | Large visual surfaces |
| `--shadow-card` | `0 18px 48px rgba(28, 62, 63, 0.12)` | Cards and image surfaces |

## Components

### Header

- Sticky header.
- Logo on the left.
- Primary CTA on the right.
- White background with subtle blur and divider.

### Lead Form

- White card with soft border.
- Two-column field layout on desktop.
- Single-column layout on tablet and mobile.
- Pill inputs.
- Required consent checkbox.
- Submit button in dark green.

Fields:

1. First Name
2. Last Name
3. Company
4. Job Title
5. Work Email
6. Phone

### Trust Pills

- Four pills in a two-column grid on desktop.
- One-column grid on mobile.
- Each pill combines logo and short label.

### Cards

- White background.
- `1px` border with `--grey-nickel`.
- `--radius-lg` border radius.
- Used for repeated information blocks.

### Dark Sections

- Background `--zen-green`.
- White headings.
- `--harp` supporting text.
- `--yellow` accents.

## Responsive Rules

### Desktop

- Hero uses two columns.
- Form fields use two columns.
- Trust pills use two columns.

### Tablet, max width 1080px

- Hero stacks into one column.
- Form fields become one column.
- Problem grid becomes two columns.

### Mobile, max width 760px

- Header is tighter.
- Logo width becomes `6.8rem`.
- H1 uses `clamp(1.95rem, 8.5vw, 2.35rem)`.
- Trust pills become one column.
- Footer content centers.

## Assets

### Brand

- `assets/brand/zen-pensions-logo.svg`
- `assets/brand/favicon-32.jpg`
- `assets/brand/cbi-logo.png`
- `assets/brand/pa-logo.svg`
- `assets/brand/state-street-logo.png`
- `assets/brand/enterprise-ireland-logo.png`
- `assets/brand/acorn-life-logo.png`

### Images

- `assets/images/workplace-team.webp`
- `assets/images/dashboard-overview.webp`
- `assets/images/employee-onboarding.webp`
- `assets/images/realtime-visibility.webp`
- `assets/images/compliance.webp`
- `assets/images/full-clarity.webp`
