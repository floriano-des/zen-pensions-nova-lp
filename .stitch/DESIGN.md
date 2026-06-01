---
name: Zen Pensions Landing Page
version: 1.0
source:
  type: static-html-css
  files:
    - index.html
    - styles.css
    - assets/brand
    - assets/images
    - assets/fonts
brand:
  product: Zen Pensions
  category: workplace pension platform
  audience: Irish employers, HR and payroll teams
  tone:
    - calm
    - regulated
    - operational
    - trustworthy
tokens:
  colors:
    white: "#ffffff"
    almost_white: "#f8faf7"
    harp: "#ebf0e9"
    cyan_mist: "#ebfefe"
    zen_green: "#1c3e3f"
    zen_green_dark: "#142d2e"
    body_blue: "#3f5372"
    light_blue: "#8c98aa"
    grey_nickel: "#bec6bb"
    pink: "#fd5e7d"
    yellow: "#ffb100"
    line_soft: "rgba(28, 62, 63, 0.16)"
  typography:
    heading_family: "Sora"
    body_family: "NotoSans"
    h1_size: "clamp(2.4rem, 4.8vw, 4.5rem)"
    h2_size: "clamp(1.85rem, 3.6vw, 3.2rem)"
    h3_size: "clamp(1.1rem, 1.6vw, 1.45rem)"
    body_size: "16px"
    strong_title_weight: 780
    light_title_weight: 360
  spacing:
    section_max: "86rem"
    section_gap: "clamp(4rem, 6vw, 5.5rem)"
    section_padding_x: "clamp(1.25rem, 4vw, 2rem)"
    hero_gap: "clamp(2rem, 4vw, 3.5rem)"
  radius:
    xl: "3rem"
    lg: "2rem"
    pill: "999px"
    lead_card: "2.2rem"
  shadows:
    soft: "0 26px 80px rgba(28, 62, 63, 0.14)"
    card: "0 18px 48px rgba(28, 62, 63, 0.12)"
---

# Zen Pensions Landing Page Design System

## Source Of Truth

This design system was extracted from the current static landing page in `index.html` and `styles.css`. The page is the source of truth. Do not introduce new visual styles, placeholder copy or invented product terminology when creating related screens.

## Visual Atmosphere

The page should feel like a serious financial product that is still simple to use. The visual language is calm, spacious and operational. It avoids marketing-heavy decoration and relies on clean hierarchy, soft green backgrounds, rounded form controls and regulatory proof points.

Primary visual signals:

- Dark green text and buttons.
- Light green page background.
- White cards with soft borders.
- Pink micro-labels for emphasis.
- Yellow accents only inside dark green sections.
- Large but controlled typography.
- Rounded inputs and CTAs.

## Color System

| Token | Value | Role |
| --- | --- | --- |
| `--white` | `#ffffff` | Cards, header, form fields |
| `--almost-white` | `#f8faf7` | Main page background |
| `--harp` | `#ebf0e9` | Soft panels and muted surfaces |
| `--cyan-mist` | `#ebfefe` | Light support surface |
| `--zen-green` | `#1c3e3f` | Primary headings, buttons, dark panels |
| `--zen-green-dark` | `#142d2e` | Button hover state |
| `--body-blue` | `#3f5372` | Paragraph text |
| `--light-blue` | `#8c98aa` | Input placeholder text |
| `--grey-nickel` | `#bec6bb` | Borders |
| `--pink` | `#fd5e7d` | Eyebrows, small labels, emphasis |
| `--yellow` | `#ffb100` | Accent on dark green panels |
| `--line-soft` | `rgba(28, 62, 63, 0.16)` | Dividers and subtle borders |

## Typography

### Font Families

- Headings, buttons, eyebrows and form labels use `Sora`.
- Body copy uses `NotoSans`.
- Font files are local:
  - `assets/fonts/sora-variable.woff2`
  - `assets/fonts/noto-sans-variable.woff2`

### Type Scale

| Element | Size | Weight | Line Height |
| --- | --- | --- | --- |
| H1 | `clamp(2.4rem, 4.8vw, 4.5rem)` | `620` base | `1.08` |
| H2 | `clamp(1.85rem, 3.6vw, 3.2rem)` | `620` base | `1.08` |
| H3 | `clamp(1.1rem, 1.6vw, 1.45rem)` | `620` | `1.08` |
| Body | `16px` | `400` | `1.45` |
| Hero body | `clamp(1rem, 1.5vw, 1.18rem)` | `400` | `1.45` |
| Eyebrow | `0.9rem` | `650` | `1.2` |
| Form label | `0.85rem` | `700` | `1.45` |
| Header CTA | `0.95rem` | `560` | `1.45` |

## Split Title Pattern

Main page titles use a two-weight structure. The first line is bold and the second line is light.

```html
<h2 class="split-title">
  <span class="title-strong">The pension was never the problem.</span>
  <span class="title-light">The old delivery model was.</span>
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

Use this pattern for H1 and major section H2 headings. Do not apply it to small card titles.

## Layout Principles

The page uses centered section shells with a maximum width and responsive gutters.

| Token | Value | Role |
| --- | --- | --- |
| `--section-max` | `86rem` | Maximum content width |
| `--section-gap` | `clamp(4rem, 6vw, 5.5rem)` | Vertical section rhythm |
| Section horizontal padding | `clamp(1.25rem, 4vw, 2rem)` | Page gutters |
| Hero gap | `clamp(2rem, 4vw, 3.5rem)` | Gap between copy and form |

Use grid layouts for hero, card groups and proof sections. Avoid floating cards inside other cards. Keep page sections unframed unless they are intentional dark panels.

## Radius And Shape

| Token | Value | Role |
| --- | --- | --- |
| `--radius-xl` | `3rem` | Large visual panels |
| `--radius-lg` | `2rem` | Cards |
| `--radius-pill` | `999px` | Buttons, inputs and pill chips |
| Lead card radius | `2.2rem` | Main form card |
| Dark workflow panel | `6rem` desktop, `2.5rem` mobile | Large campaign block |

## Shadows

| Token | Value | Role |
| --- | --- | --- |
| `--shadow-soft` | `0 26px 80px rgba(28, 62, 63, 0.14)` | Large visual surfaces |
| `--shadow-card` | `0 18px 48px rgba(28, 62, 63, 0.12)` | Cards and image panels |

## Component Patterns

### Header

- Sticky top header.
- White translucent background with subtle blur.
- Logo on the left.
- Pill CTA on the right.
- CTA uses `--zen-green` and white text.

### Hero

- Two-column layout on desktop.
- Left side: eyebrow, split H1, supporting copy and trust pills.
- Right side: lead form card.
- Large workplace image spans below both columns.

### Lead Form

The form follows the Zen Pensions reference style.

- White card.
- Soft green page background around it.
- Pill inputs.
- Two-column fields on desktop.
- One-column fields on tablet and mobile.
- Consent checkbox spans full width.
- Submit button uses dark green fill.

Fields:

1. First Name
2. Last Name
3. Company
4. Job Title
5. Work Email
6. Phone
7. Consent checkbox

### Trust Pills

- Four pill cards.
- Two columns on desktop.
- One column on mobile.
- Each item includes a brand mark and a short label.
- Labels: Central Bank regulated, Pensions Authority approved, Assets held by State Street, Backed by Enterprise Ireland.

### Problem Cards

- Four cards.
- White background.
- Grey nickel border.
- Pink number label.
- Dark green card title.
- Body copy in body blue.

### Dark Panels

Use dark green panels for urgency or process sections.

- Background: `--zen-green`.
- Heading: white.
- Body copy: `--harp`.
- Eyebrow and step badges: `--yellow`.

### Footer

- White background.
- Logo left.
- Legal text, links and regulatory marks right.
- Content centers on mobile.

## Responsive Behavior

### Desktop

- Hero has two columns.
- Lead form uses two field columns.
- Trust pills use two columns.
- Product grid uses mixed large and regular cards.

### Tablet, max width 1080px

- Hero stacks to one column.
- Form fields become one column.
- Problem grid becomes two columns.
- Product and stakeholder cards stack.

### Mobile, max width 760px

- Header becomes compact.
- Logo width becomes `6.8rem`.
- H1 uses `clamp(1.95rem, 8.5vw, 2.35rem)`.
- Trust pills become one column.
- Footer content centers.

## Content And Terminology

Use existing page language as the content source. Important terms include:

- Zen Pensions.
- Irish employers.
- workplace pensions.
- My Future Fund.
- Central Bank regulated.
- Pensions Authority approved.
- Assets held by State Street.
- Backed by Enterprise Ireland.
- Book a Call.

Do not replace these with generic SaaS terminology.

## Assets

### Brand

- `assets/brand/zen-pensions-logo.svg`
- `assets/brand/favicon-32.jpg`
- `assets/brand/cbi-logo.png`
- `assets/brand/pa-logo.svg`
- `assets/brand/state-street-logo.png`
- `assets/brand/enterprise-ireland-logo.png`
- `assets/brand/acorn-life-logo.png`

### Imagery

- `assets/images/workplace-team.webp`
- `assets/images/dashboard-overview.webp`
- `assets/images/employee-onboarding.webp`
- `assets/images/realtime-visibility.webp`
- `assets/images/compliance.webp`
- `assets/images/full-clarity.webp`

## Stitch Guidance

When importing into Stitch, use this file as the design system reference. If Stitch expects a project-level design system file, copy this file to `.stitch/DESIGN.md`.
