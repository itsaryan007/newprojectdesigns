# New Project Designs Design System

Version: 1.0  
Purpose: Website design system for New Project Designs, based on the finalized yellow and green editorial direction across these screens:

1. Curated for Your Event
2. Signage & Print Shop
3. Vinyl Printing Product Page

---

## 1. Brand Direction

New Project Designs should feel:

- Editorial
- Curated
- Premium
- Event-focused
- Custom-made
- Warm
- Artistic but usable
- Clean, not sterile
- Elevated, not luxury-cold
- Visual-first, not form-heavy

The design should avoid looking like:

- A generic ecommerce template
- A SaaS dashboard
- A dark-gradient shop page
- An Etsy clone
- A wedding template overloaded with script fonts
- A plain Shopify grid with no brand personality

---

## 2. Core Visual Principles

### Use

- Cream backgrounds instead of pure white
- Deep sage green as the main brand color
- Warm yellow as the accent color
- Large typography with clear hierarchy
- Rounded cards
- Soft shadows
- Thin botanical line art
- Thin geometric lines
- Editorial image layouts
- Consistent warm photography
- Spacious layouts

### Avoid

- Pure white page backgrounds
- Pure black text unless necessary
- Dark gradients
- Bright neon colors
- Heavy borders
- Gray admin-style forms
- Dense layouts
- Random font combinations
- Busy photo backgrounds
- Overly colorful icons
- Harsh shadows

---

# 3. Font System

The screenshots are image mockups, so exact font metadata is not available. Use this font system to recreate the aesthetic.

## Recommended Font Imports

```css
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Cormorant+Garamond:wght@400;500;600;700&family=Inter:wght@400;500;600;700&display=swap");
```

## Font Roles

| Use Case | Font | Weight | Notes |
|---|---|---:|---|
| Logo | Existing logo image or SVG | N/A | Do not recreate logo as live text unless necessary |
| Editorial Hero Titles | Cormorant Garamond | 600 | Used on Signage & Print Shop and Vinyl Printing pages |
| Editorial Section Titles | Cormorant Garamond | 500 / 600 | Used for section headings |
| Impact Display Titles | Bebas Neue | 400 | Used on “Curated for Your Event” |
| Category Card Titles | Bebas Neue | 400 | Used on green/yellow cards |
| Body Text | Inter | 400 | Clean readable text |
| Navigation | Inter | 500 / 600 | Small and minimal |
| Labels / Overlines | Inter | 700 | Uppercase with wide letter spacing |
| Buttons / CTAs | Inter | 600 | Simple and clear |

## Font Tokens

```css
:root {
  --font-serif: "Cormorant Garamond", Georgia, serif;
  --font-sans: "Inter", Arial, sans-serif;
  --font-display: "Bebas Neue", Impact, sans-serif;
}
```

---

# 4. Typography Scale

## Desktop Typography

| Token | Font | Size | Line Height | Weight | Letter Spacing | Usage |
|---|---|---:|---:|---:|---:|---|
| `display-impact-xl` | Bebas Neue | 104px | 0.88 | 400 | 0.01em | “Curated for Your Event” title |
| `display-impact-lg` | Bebas Neue | 72px | 0.92 | 400 | 0.01em | Large category headers |
| `h1-editorial` | Cormorant Garamond | 64px | 66px | 600 | -0.02em | Product/shop hero titles |
| `h2-editorial` | Cormorant Garamond | 44px | 50px | 500 | -0.01em | Section headings |
| `h3-editorial` | Cormorant Garamond | 34px | 40px | 500 | -0.01em | Product card titles |
| `card-title-display` | Bebas Neue | 42px | 42px | 400 | 0.01em | Green/yellow category card titles |
| `body-lg` | Inter | 18px | 30px | 400 | 0 | Hero subtitles |
| `body-md` | Inter | 16px | 26px | 400 | 0 | Main body copy |
| `body-sm` | Inter | 14px | 22px | 400 | 0 | Helper text |
| `label` | Inter | 14px | 18px | 700 | 0.18em | Uppercase labels |
| `nav` | Inter | 14px | 20px | 500 | 0 | Navigation |
| `button` | Inter | 14px | 18px | 600 | 0.02em | Buttons and CTAs |

## Tablet Typography

| Token | Size | Line Height |
|---|---:|---:|
| `display-impact-xl` | 78px | 0.9 |
| `display-impact-lg` | 60px | 0.94 |
| `h1-editorial` | 54px | 58px |
| `h2-editorial` | 38px | 44px |
| `h3-editorial` | 30px | 36px |
| `card-title-display` | 36px | 38px |
| `body-lg` | 17px | 28px |
| `body-md` | 16px | 26px |
| `body-sm` | 14px | 22px |
| `label` | 13px | 18px |

## Mobile Typography

| Token | Size | Line Height |
|---|---:|---:|
| `display-impact-xl` | 56px | 0.92 |
| `display-impact-lg` | 44px | 0.96 |
| `h1-editorial` | 42px | 46px |
| `h2-editorial` | 32px | 38px |
| `h3-editorial` | 28px | 34px |
| `card-title-display` | 32px | 34px |
| `body-lg` | 16px | 26px |
| `body-md` | 15px | 24px |
| `body-sm` | 13px | 21px |
| `label` | 12px | 16px |
| `nav` | 14px | 20px |
| `button` | 14px | 18px |

---

# 5. Color System

## CSS Variables

```css
:root {
  /* Backgrounds */
  --color-cream: #F7F3EA;
  --color-cream-soft: #FBF8F0;
  --color-card-cream: #F9F4E8;

  /* Greens */
  --color-green-900: #2F5138;
  --color-green-800: #3F6848;
  --color-green-700: #4E7654;
  --color-green-600: #5F8763;
  --color-sage-line: #789177;
  --color-sage-soft: #E8EEE4;

  /* Yellows */
  --color-yellow-700: #B89632;
  --color-yellow-600: #D7B94E;
  --color-yellow-500: #F3D36D;
  --color-yellow-400: #F7DA81;
  --color-yellow-200: #F9E7B5;
  --color-yellow-soft: #FFF1C8;

  /* Text */
  --color-text-primary: #1F1D1A;
  --color-text-secondary: #4F5A4D;
  --color-text-muted: #6D716A;
  --color-text-inverse: #FBF8F0;

  /* Borders */
  --color-border-light: #DDD5C6;
  --color-border-green: #6F8E72;
  --color-border-yellow: #E8C762;

  /* Functional */
  --color-success: #4E7654;
  --color-warning: #F3D36D;
  --color-error: #9B3A2F;
}
```

## Color Usage

| Element | Color |
|---|---|
| Page background | `--color-cream` |
| Soft sections | `--color-cream-soft` |
| Neutral cards | `--color-card-cream` |
| Green cards | `--color-green-700` |
| Footer / trust strip | `--color-green-800` |
| Primary buttons | `--color-green-800` |
| Primary button hover | `--color-green-900` |
| Yellow cards | `--color-yellow-500` |
| Size card footer | `--color-yellow-200` |
| Rush strip | `--color-yellow-soft` |
| Main text | `--color-text-primary` |
| Secondary text | `--color-text-secondary` |
| Muted text | `--color-text-muted` |
| Text on green | `--color-text-inverse` or `--color-yellow-500` |
| Line art | `--color-sage-line` at 30% to 55% opacity |
| Active border | `--color-green-800` |
| Default border | `--color-border-light` |

---

# 6. Layout System

## Containers

```css
:root {
  --container-xl: 1280px;
  --container-lg: 1120px;
  --container-md: 960px;
}
```

| Breakpoint | Container Padding |
|---|---:|
| Large desktop | 80px |
| Desktop | 64px |
| Tablet | 32px |
| Mobile | 20px |

## Grid

| Device | Grid |
|---|---|
| Desktop | 12 columns |
| Tablet | 8 columns |
| Mobile | 4 columns |

## Common Gaps

| Token | Size |
|---|---:|
| `gap-xs` | 8px |
| `gap-sm` | 12px |
| `gap-md` | 20px |
| `gap-lg` | 24px |
| `gap-xl` | 32px |
| `gap-2xl` | 48px |
| `gap-3xl` | 64px |

## Section Spacing

| Token | Desktop | Tablet | Mobile |
|---|---:|---:|---:|
| `section-xl` | 120px | 96px | 72px |
| `section-lg` | 96px | 80px | 56px |
| `section-md` | 72px | 56px | 48px |
| `section-sm` | 48px | 40px | 32px |

## Base Layout CSS

```css
body {
  margin: 0;
  background: var(--color-cream);
  color: var(--color-text-primary);
  font-family: var(--font-sans);
  font-size: 16px;
  line-height: 1.6;
}

.container {
  width: min(100% - 128px, var(--container-xl));
  margin-inline: auto;
}

.section {
  padding-block: 96px;
}

@media (max-width: 1024px) {
  .container {
    width: min(100% - 64px, var(--container-md));
  }

  .section {
    padding-block: 72px;
  }
}

@media (max-width: 640px) {
  .container {
    width: min(100% - 40px, 100%);
  }

  .section {
    padding-block: 56px;
  }
}
```

---

# 7. Border Radius

```css
:root {
  --radius-xs: 6px;
  --radius-sm: 8px;
  --radius-md: 8px; /* Standardized for inputs/textboxes */
  --radius-lg: 16px;
  --radius-xl: 24px; /* Standardized for buttons */
  --radius-pill: 24px; /* Updated for standardized 24px button look */
}
```

| Element | Radius |
|---|---:|
| Small badges | `--radius-pill` |
| Buttons | `--radius-xl` (24px) |
| Inputs / Text boxes | `--radius-md` (8px) |
| Product cards | `--radius-lg` (16px) |
| Category cards | `--radius-lg` to `--radius-xl` |
| Image thumbnails | `--radius-sm` (8px) |
| Upload zones | `--radius-sm` (8px) |
| Info strips | `--radius-sm` (8px) |
| Footer strip | `0` |

---

# 8. Shadows

Use soft shadows only. Nothing should feel like a dashboard card from an abandoned HR portal.

```css
:root {
  --shadow-card: 0 12px 30px rgba(47, 81, 56, 0.12);
  --shadow-card-soft: 0 8px 22px rgba(31, 29, 26, 0.08);
  --shadow-hover: 0 16px 36px rgba(47, 81, 56, 0.16);
}
```

| Element | Shadow |
|---|---|
| Default card | `--shadow-card-soft` |
| Featured card | `--shadow-card` |
| Hover card | `--shadow-hover` |
| Navigation | none |
| Footer / trust strip | none |

---

# 9. Navigation

## Desktop Header Specs

| Property | Value |
|---|---|
| Height | 92px |
| Background | `--color-cream` |
| Logo width | 145px |
| Nav font | Inter 14px Medium |
| Nav color | `--color-text-primary` |
| Active underline | 1px solid `--color-green-800` |
| Icon button size | 38px |
| Icon button shape | Circle |
| Header CTA height | 40px |
| Header CTA padding | 18px 22px |
| Header CTA radius | Pill |

## Navigation CSS

```css
.site-header {
  height: 92px;
  background: var(--color-cream);
  display: flex;
  align-items: center;
  border-bottom: 1px solid rgba(120, 145, 119, 0.25);
}

.site-logo {
  width: 145px;
  height: auto;
}

.nav-link {
  font-family: var(--font-sans);
  font-size: 14px;
  font-weight: 500;
  color: var(--color-text-primary);
  text-decoration: none;
  padding-bottom: 6px;
}

.nav-link.active {
  border-bottom: 1px solid var(--color-green-800);
}

.nav-icon {
  width: 38px;
  height: 38px;
  border-radius: 999px;
  background: #08190F;
  color: var(--color-text-inverse);
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

.nav-cta {
  height: 40px;
  padding: 0 22px;
  border-radius: var(--radius-pill);
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  font-family: var(--font-sans);
  font-size: 14px;
  font-weight: 600;
  border: 0;
}
```

---

# 10. Hero Styles

There are two hero styles.

## A. Impact Hero

Used for:

- Curated for Your Event

```css
.hero-impact {
  text-align: center;
  position: relative;
}

.hero-impact-label {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 18px;
  font-weight: 700;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--color-green-800);
}

.hero-impact-title {
  font-family: var(--font-display);
  font-size: 104px;
  line-height: 0.88;
  font-weight: 400;
  letter-spacing: 0.01em;
  text-transform: uppercase;
  color: var(--color-green-700);
  text-align: center;
  margin: 16px 0 24px;
}

.hero-impact-subtitle {
  font-family: var(--font-sans);
  font-size: 18px;
  line-height: 30px;
  font-weight: 400;
  color: var(--color-text-secondary);
  max-width: 560px;
  margin-inline: auto;
}
```

## B. Editorial Hero

Used for:

- Signage & Print Shop
- Vinyl Printing Product Page

```css
.hero-editorial {
  text-align: center;
  position: relative;
}

.hero-editorial-label {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 18px;
  font-weight: 700;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--color-green-800);
}

.hero-editorial-title {
  font-family: var(--font-serif);
  font-size: 64px;
  line-height: 66px;
  font-weight: 600;
  letter-spacing: -0.02em;
  color: var(--color-text-primary);
  text-align: center;
  max-width: 780px;
  margin: 18px auto 0;
}

.hero-editorial-divider {
  width: 64px;
  height: 1px;
  background: var(--color-green-800);
  margin: 28px auto;
}

.hero-editorial-subtitle {
  font-family: var(--font-sans);
  font-size: 18px;
  line-height: 30px;
  font-weight: 400;
  color: var(--color-text-secondary);
  max-width: 540px;
  margin-inline: auto;
}
```

---

# 11. Decorative Line Art

Use thin decorative line art as background accents.

## Approved Decorative Elements

- Botanical branch
- Sunburst
- Oversized arc
- Thin vertical grid lines
- Thin horizontal grid lines
- Small leaf badge
- Small sparkle badge

## Decoration Rules

| Property | Value |
|---|---|
| Stroke width | 1px |
| Color | `--color-sage-line` |
| Opacity | 30% to 55% |
| Placement | Edges and corners |
| Behavior | Decorative only |
| Accessibility | Should not carry meaning |
| Text overlap | Avoid placing behind important text |

## CSS Example

```css
.decor-line {
  position: absolute;
  pointer-events: none;
  stroke: var(--color-sage-line);
  opacity: 0.45;
  stroke-width: 1;
}

.decor-line.subtle {
  opacity: 0.3;
}
```

---

# 12. Buttons and CTAs

## Primary Button

```css
.button-primary {
  height: 52px;
  padding: 0 32px;
  border-radius: var(--radius-pill);
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  border: 0;
  font-family: var(--font-sans);
  font-size: 15px;
  font-weight: 600;
  letter-spacing: 0.02em;
  cursor: pointer;
}

.button-primary:hover {
  background: var(--color-green-900);
}
```

## Secondary Button

```css
.button-secondary {
  height: 52px;
  padding: 0 32px;
  border-radius: var(--radius-pill);
  background: transparent;
  color: var(--color-green-800);
  border: 1px solid var(--color-green-800);
  font-family: var(--font-sans);
  font-size: 15px;
  font-weight: 600;
  cursor: pointer;
}

.button-secondary:hover {
  background: rgba(63, 104, 72, 0.08);
}
```

## Text CTA

```css
.text-cta {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  font-family: var(--font-sans);
  font-size: 15px;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: var(--color-green-800);
  text-decoration: none;
}
```

## Add to Cart Button

```css
.add-to-cart {
  width: 100%;
  height: 58px;
  border-radius: 10px;
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  border: 0;
  font-family: var(--font-sans);
  font-size: 17px;
  font-weight: 600;
  cursor: pointer;
}

.add-to-cart:hover {
  background: var(--color-green-900);
}
```

---

# 13. Cards

## Base Card

```css
.card {
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-card-soft);
  overflow: hidden;
  background: var(--color-cream-soft);
}

.card:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-hover);
  transition: transform 180ms ease, box-shadow 180ms ease;
}
```

## Image Rules for Cards

```css
.card-image {
  width: 100%;
  display: block;
  object-fit: cover;
}
```

Recommended ratios:

| Use Case | Ratio |
|---|---|
| Category card image | 4:3 |
| Product card image | 16:10 |
| Gallery image | 5:4 |
| Size selection image | 4:3 |
| Mobile card image | 4:3 |

---

# 14. Curated for Your Event Page

## Purpose

This page introduces high-level shop categories in a bold editorial way.

## Content Structure

```txt
Label: SHOP EVENT DETAILS
Title: CURATED FOR YOUR EVENT
Subtitle: Thoughtfully designed pieces and custom details to bring your vision to life.

Cards:
1. Signage & Vinyl
2. Event Menus & Paper
3. Gifts & Add-ons

Bottom trust strip:
- Custom Made
- Event Ready
- Made With Intention
```

## Layout

| Element | Desktop |
|---|---:|
| Hero top padding | 80px |
| Hero bottom spacing | 56px |
| Card grid | 3 columns |
| Card gap | 32px |
| Card height | 470px to 520px |
| Card padding | 24px |
| Image height | 210px to 230px |

## Curated Category Card

```css
.category-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

.category-card {
  min-height: 500px;
  border-radius: var(--radius-xl);
  padding: 24px;
  box-shadow: var(--shadow-card);
  overflow: hidden;
  position: relative;
}

.category-card-image {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: var(--radius-md);
  margin-bottom: 28px;
}

.category-card-title {
  font-family: var(--font-display);
  font-size: 42px;
  line-height: 42px;
  font-weight: 400;
  letter-spacing: 0.01em;
  text-transform: uppercase;
  margin: 0 0 16px;
}

.category-card-body {
  font-family: var(--font-sans);
  font-size: 16px;
  line-height: 26px;
  margin: 0 0 28px;
  max-width: 310px;
}
```

## Green Card Variant

```css
.category-card.green {
  background: var(--color-green-700);
  color: var(--color-yellow-500);
}

.category-card.green .text-cta {
  color: var(--color-yellow-500);
}
```

Use for:

- Signage & Vinyl
- Gifts & Add-ons

## Yellow Card Variant

```css
.category-card.yellow {
  background: var(--color-yellow-500);
  color: var(--color-green-800);
}

.category-card.yellow .text-cta {
  color: var(--color-green-800);
}
```

Use for:

- Event Menus & Paper

## Thumbnail Direction

| Category | Thumbnail Direction |
|---|---|
| Signage & Vinyl | Acrylic sign or vinyl sign in a styled event setup |
| Event Menus & Paper | Menu card, paper goods, table setting |
| Gifts & Add-ons | Gift tag, favor box, ribbon, styled detail shot |

Image style:

- Warm natural lighting
- Cream, green, yellow, beige tones
- Minimal clutter
- Soft shadows
- Close enough to show detail
- No random phone snapshots
- No heavy filters
- No harsh flash

---

# 15. Signage & Print Shop Page

## Purpose

This page routes users into the right product category.

## Content Structure

```txt
Hero:
Label: SIGNAGE & PRINT SHOP
Title: Custom Signage, Vinyl & Event Details
Subtitle: Designed to elevate your event with modern, custom-made pieces.

Cards:
1. Acrylic & Vinyl Signage
2. Vinyl Printing

How It Works:
1. Choose Your Product
2. Customize or Upload
3. We Print & Prepare

Bottom CTA:
Need something custom?
Start a Custom Inquiry
```

## Layout

| Element | Desktop |
|---|---:|
| Hero top padding | 90px |
| Hero bottom spacing | 72px |
| Product card grid | 2 columns |
| Product card gap | 32px |
| Product card min height | 680px |
| Product card image height | 330px |
| Product card content padding | 40px |

## Product Category Cards

```css
.product-category-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 32px;
}

.product-category-card {
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-card-soft);
  background: var(--color-cream-soft);
}

.product-category-card-image {
  width: 100%;
  height: 330px;
  object-fit: cover;
}

.product-category-card-content {
  padding: 40px;
}

.product-category-card-title {
  font-family: var(--font-serif);
  font-size: 38px;
  line-height: 44px;
  font-weight: 500;
  letter-spacing: -0.01em;
  color: var(--color-text-primary);
  margin: 0 0 18px;
}

.product-category-card-body {
  font-family: var(--font-sans);
  font-size: 16px;
  line-height: 28px;
  color: var(--color-text-secondary);
  margin: 0 0 32px;
}
```

## Acrylic Card

```css
.product-category-card.acrylic {
  background: var(--color-cream-soft);
}
```

Thumbnail:

- Acrylic sign on stand
- Neutral tabletop
- Soft plant shadow
- Cream background
- Minimal styling

## Vinyl Card

```css
.product-category-card.vinyl {
  background: linear-gradient(180deg, var(--color-yellow-soft), var(--color-yellow-200));
}
```

Thumbnail:

- Vinyl text being applied
- Close-up of hand and material
- Soft neutral fabric or wall
- Green lettering preferred

---

# 16. How It Works Section

Used on Signage & Print Shop page.

## Structure

```txt
Label: HOW IT WORKS
Title: Simple steps. Beautiful results.

Steps:
1. Choose Your Product
2. Customize or Upload
3. We Print & Prepare
```

## CSS

```css
.how-it-works {
  background: rgba(251, 248, 240, 0.75);
  border-radius: var(--radius-xl);
  padding: 64px 56px;
  text-align: center;
}

.how-label {
  font-family: var(--font-sans);
  font-size: 14px;
  font-weight: 700;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--color-green-800);
}

.how-title {
  font-family: var(--font-serif);
  font-size: 42px;
  line-height: 48px;
  font-weight: 500;
  color: var(--color-text-primary);
  margin: 14px 0 48px;
}

.how-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 48px;
}

.how-step-title {
  font-family: var(--font-serif);
  font-size: 22px;
  line-height: 28px;
  font-weight: 500;
  color: var(--color-text-primary);
}

.how-step-body {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 24px;
  color: var(--color-text-secondary);
}
```

---

# 17. Vinyl Printing Product Page

## Purpose

This page should feel like a premium product configurator, not a boring form.

## Content Structure

```txt
Back to Shop

Hero:
Label: VINYL PRINTING
Title: Custom Vinyl Prints, Made for Your Event
Subtitle: Choose your size, upload your artwork, and we'll handle the rest with precision and care.

Step 1:
Select Your Size

Size cards:
1. 2' x 2' - $80 minimum
2. 2' x 3' - $95 minimum
3. 3' x 4' - $144

Step 2:
Upload Your Artwork

Side card:
File Guidelines

Rush Production:
+30%, 3-5 day turnaround

Add to Cart

Before You Order

Real Projects Gallery

Bottom Trust Strip:
- Custom Made
- Event Ready
- Made With Intention
```

## Layout

| Element | Desktop |
|---|---:|
| Page max width | 1280px |
| Size grid | 3 columns |
| Size card gap | 24px |
| Upload layout | 2 columns |
| Upload main column | 2fr |
| Guidelines card | 1fr |
| Gallery grid | 5 columns |

---

## Step Header

```css
.step-header {
  display: flex;
  align-items: center;
  gap: 14px;
  margin-bottom: 22px;
}

.step-badge {
  width: 32px;
  height: 32px;
  border-radius: var(--radius-pill);
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-sans);
  font-size: 14px;
  font-weight: 700;
}

.step-title {
  font-family: var(--font-serif);
  font-size: 26px;
  line-height: 32px;
  font-weight: 500;
  color: var(--color-text-primary);
  margin: 0;
}
```

---

## Size Selection Cards

```css
.size-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.size-card {
  border-radius: 16px;
  overflow: hidden;
  background: var(--color-cream-soft);
  border: 1px solid var(--color-border-light);
  box-shadow: var(--shadow-card-soft);
  cursor: pointer;
}

.size-card:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-hover);
}

.size-card.selected {
  border: 2px solid var(--color-green-800);
}

.size-card-image {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.size-card-footer {
  background: var(--color-yellow-200);
  padding: 28px;
  text-align: center;
}

.size-title {
  font-family: var(--font-serif);
  font-size: 34px;
  line-height: 38px;
  font-weight: 600;
  color: var(--color-text-primary);
  margin: 0 0 6px;
}

.size-price {
  font-family: var(--font-sans);
  font-size: 16px;
  line-height: 24px;
  color: var(--color-text-primary);
  margin: 0 0 18px;
}

.size-cta {
  font-family: var(--font-sans);
  font-size: 15px;
  font-weight: 600;
  color: var(--color-green-800);
}
```

## Selected State

```css
.size-selected-icon {
  width: 38px;
  height: 38px;
  border-radius: var(--radius-pill);
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  display: inline-flex;
  align-items: center;
  justify-content: center;
}
```

## Size Card Thumbnail Direction

| Size | Thumbnail Direction |
|---|---|
| 2' x 2' | Small acrylic or circular sign with close-up styling |
| 2' x 3' | Medium event panel or wall signage with florals |
| 3' x 4' | Large backdrop or wall vinyl in an event room |

Image requirements:

- Use scale references when possible
- Show real event context
- Keep the palette cream, green, beige, yellow
- Avoid cluttered background scenes
- Avoid dark lighting
- Avoid random mockup placeholders

---

## Upload Artwork Section

```css
.upload-layout {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 24px;
  align-items: stretch;
}

.upload-area {
  min-height: 240px;
  border-radius: var(--radius-md);
  border: 1.5px dashed var(--color-green-700);
  background: var(--color-cream-soft);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 32px;
}

.upload-icon {
  color: var(--color-green-800);
  margin-bottom: 16px;
}

.upload-title {
  font-family: var(--font-sans);
  font-size: 16px;
  line-height: 24px;
  color: var(--color-text-secondary);
  margin-bottom: 16px;
}

.upload-helper {
  font-family: var(--font-sans);
  font-size: 13px;
  line-height: 20px;
  color: var(--color-text-muted);
  margin-top: 18px;
}
```

## Choose File Button

```css
.choose-file-button {
  height: 42px;
  padding: 0 26px;
  border-radius: var(--radius-pill);
  border: 0;
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  font-family: var(--font-sans);
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
}
```

---

## File Guidelines Card

```css
.guidelines-card {
  border-radius: var(--radius-md);
  background: var(--color-card-cream);
  padding: 32px;
  box-shadow: var(--shadow-card-soft);
}

.guidelines-title {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 18px;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--color-green-800);
  margin-bottom: 18px;
}

.guidelines-list {
  margin: 0;
  padding-left: 0;
  list-style: none;
}

.guidelines-list li {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 24px;
  color: var(--color-text-primary);
}
```

## File Guidelines Copy

```txt
High resolution (300 DPI)
PDF, PNG, or JPEG
CMYK color mode preferred
Convert text to outlines
```

## Custom Size Copy

```txt
Need a custom size?
Email or message us and we'll create a custom order just for you.
```

---

## Rush Production Strip

```css
.rush-strip {
  background: var(--color-yellow-soft);
  border-radius: var(--radius-md);
  padding: 22px 28px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.rush-title {
  font-family: var(--font-serif);
  font-size: 22px;
  line-height: 28px;
  font-weight: 500;
  color: var(--color-text-primary);
  margin: 0;
}

.rush-body {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 22px;
  color: var(--color-text-primary);
  margin: 2px 0 0;
}
```

## Toggle

```css
.toggle {
  width: 52px;
  height: 30px;
  border-radius: var(--radius-pill);
  background: rgba(63, 104, 72, 0.2);
  position: relative;
}

.toggle::after {
  content: "";
  width: 26px;
  height: 26px;
  border-radius: var(--radius-pill);
  background: var(--color-cream-soft);
  position: absolute;
  top: 2px;
  left: 2px;
  box-shadow: var(--shadow-card-soft);
}

.toggle.active {
  background: var(--color-green-800);
}

.toggle.active::after {
  left: 24px;
}
```

---

## Before You Order Strip

```css
.before-order {
  background: var(--color-card-cream);
  border-radius: var(--radius-md);
  padding: 24px 32px;
  display: grid;
  grid-template-columns: 1.2fr repeat(4, 1fr);
  gap: 24px;
  align-items: center;
  box-shadow: var(--shadow-card-soft);
}

.before-order-title {
  font-family: var(--font-serif);
  font-size: 22px;
  line-height: 28px;
  font-weight: 500;
  color: var(--color-text-primary);
}

.before-order-item {
  font-family: var(--font-sans);
  font-size: 13px;
  line-height: 20px;
  color: var(--color-text-primary);
  text-align: center;
}
```

## Before You Order Copy

```txt
Minimum $95 per order.
7-day standard turnaround.
Pickup at our location in Anaheim, CA.
Add to a rental order for delivery options.
Questions? Visit our contact page.
```

---

## Real Projects Gallery

```css
.project-gallery {
  text-align: center;
}

.project-gallery-title {
  font-family: var(--font-serif);
  font-size: 36px;
  line-height: 42px;
  font-weight: 500;
  color: var(--color-text-primary);
  margin: 0 0 6px;
}

.project-gallery-subtitle {
  font-family: var(--font-sans);
  font-size: 14px;
  line-height: 22px;
  color: var(--color-text-secondary);
  margin: 0 0 28px;
}

.project-gallery-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 20px;
}

.project-gallery-image {
  width: 100%;
  aspect-ratio: 5 / 4;
  object-fit: cover;
  border-radius: var(--radius-md);
}
```

## Gallery Image Direction

Use images that show:

- Vinyl wall text
- Acrylic signs
- Welcome signs
- Bar signs
- Menu prints
- Styled event installations
- Large wall wraps
- Real event setups

Avoid:

- Product-only cutouts on white
- Low-quality phone photos
- Cropped text
- Dark backgrounds
- Overly busy decor
- Inconsistent filters

---

# 18. Trust Strip

Used at the bottom of the Curated page and Vinyl Printing page.

## Content

```txt
Custom Made
Event Ready
Made With Intention
```

## CSS

```css
.trust-strip {
  min-height: 76px;
  background: var(--color-green-800);
  color: var(--color-text-inverse);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 64px;
  padding: 20px 32px;
}

.trust-strip-item {
  display: inline-flex;
  align-items: center;
  gap: 14px;
  font-family: var(--font-sans);
  font-size: 15px;
  line-height: 20px;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.trust-strip-divider {
  width: 1px;
  height: 32px;
  background: rgba(251, 248, 240, 0.45);
}
```

---

# 19. Icon System

## Icon Style

| Property | Value |
|---|---|
| Style | Thin outline |
| Stroke width | 1.5px |
| Color on light background | `--color-green-800` |
| Color on green background | `--color-text-inverse` or `--color-yellow-500` |
| Icon circle size | 54px |
| Icon circle background | `--color-cream-soft` or transparent |

## Approved Icons

- Leaf
- Vase
- Sparkle
- Cart
- Upload cloud
- Printer
- Document
- Lightning
- Box
- Arrow
- Checkmark

## Avoid

- Emoji-style icons
- Filled colorful icons
- Generic SaaS icons
- Icons with multiple colors
- Heavy icon strokes

---

# 20. Image System

## General Photography Direction

All images should feel like they belong to the same styled shoot.

| Rule | Direction |
|---|---|
| Lighting | Warm natural light |
| Color | Cream, green, beige, soft yellow |
| Contrast | Soft but clear |
| Cropping | Product or event object clearly framed |
| Background | Minimal, styled, premium |
| Texture | Paper, acrylic, fabric, floral, soft shadows |
| Mood | Calm, curated, thoughtful |

## Avoid

- Harsh flash
- Dark room photos
- Overly saturated balloons
- Busy backgrounds
- Random crops
- Mixed filters
- Heavy black shadows
- Overly sharp contrast
- Low-resolution uploads

## Image Ratios

| Use Case | Ratio |
|---|---|
| Category card image | 4:3 |
| Product card hero image | 16:10 |
| Gallery thumbnail | 5:4 |
| Size selection image | 4:3 |
| Mobile card image | 4:3 |

---

# 21. Form Styling

Forms should feel warm and branded, not like an abandoned checkout page.

## Inputs

```css
.input {
  height: 52px;
  border-radius: var(--radius-pill);
  border: 1px solid var(--color-border-light);
  background: var(--color-cream-soft);
  color: var(--color-text-primary);
  font-family: var(--font-sans);
  font-size: 15px;
  padding: 0 20px;
}

.input:focus {
  outline: none;
  border-color: var(--color-green-800);
  box-shadow: 0 0 0 3px rgba(63, 104, 72, 0.12);
}

.textarea {
  min-height: 140px;
  border-radius: var(--radius-md);
  border: 1px solid var(--color-border-light);
  background: var(--color-cream-soft);
  color: var(--color-text-primary);
  font-family: var(--font-sans);
  font-size: 15px;
  line-height: 24px;
  padding: 18px 20px;
}
```

## Labels

```css
.form-label {
  font-family: var(--font-sans);
  font-size: 13px;
  line-height: 18px;
  font-weight: 600;
  color: var(--color-green-800);
  margin-bottom: 8px;
}
```

---

# 22. Responsive Rules

## Desktop

- Use max container width of 1280px.
- Curated category cards use 3 columns.
- Signage shop cards use 2 columns.
- Vinyl size cards use 3 columns.
- Vinyl upload section uses 2 columns.
- Gallery uses 5 columns.

## Tablet

- Curated category cards can become 2 columns.
- Product cards can remain 2 columns if width allows.
- Vinyl size cards can become 2 columns.
- Upload and guidelines can remain 2 columns if readable.
- Hero titles scale down.

## Mobile

- All cards stack to 1 column.
- Hero titles remain centered.
- Section padding reduces.
- Navigation collapses.
- Upload and guidelines stack.
- Trust strip stacks vertically or becomes horizontal scroll.
- Gallery becomes 2 columns or horizontal scroll.
- Decorative line art should be reduced or hidden.

## Responsive CSS

```css
@media (max-width: 1024px) {
  .category-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .size-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .project-gallery-grid {
    grid-template-columns: repeat(3, 1fr);
  }

  .hero-impact-title {
    font-size: 78px;
  }

  .hero-editorial-title {
    font-size: 54px;
    line-height: 58px;
  }
}

@media (max-width: 768px) {
  .product-category-grid,
  .upload-layout,
  .how-grid,
  .before-order {
    grid-template-columns: 1fr;
  }

  .trust-strip {
    flex-direction: column;
    gap: 20px;
  }

  .trust-strip-divider {
    display: none;
  }
}

@media (max-width: 640px) {
  .category-grid,
  .size-grid {
    grid-template-columns: 1fr;
  }

  .project-gallery-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .hero-impact-title {
    font-size: 56px;
    line-height: 0.92;
  }

  .hero-editorial-title {
    font-size: 42px;
    line-height: 46px;
  }

  .category-card-title {
    font-size: 32px;
    line-height: 34px;
  }
}
```

---

# 23. Tailwind Configuration Reference

Use this when implementing in Tailwind.

```js
theme: {
  extend: {
    colors: {
      cream: "#F7F3EA",
      creamSoft: "#FBF8F0",
      cardCream: "#F9F4E8",

      green900: "#2F5138",
      green800: "#3F6848",
      green700: "#4E7654",
      green600: "#5F8763",
      sageLine: "#789177",
      sageSoft: "#E8EEE4",

      yellow700: "#B89632",
      yellow600: "#D7B94E",
      yellow500: "#F3D36D",
      yellow400: "#F7DA81",
      yellow200: "#F9E7B5",
      yellowSoft: "#FFF1C8",

      textPrimary: "#1F1D1A",
      textSecondary: "#4F5A4D",
      textMuted: "#6D716A",
      textInverse: "#FBF8F0",

      borderLight: "#DDD5C6",
      borderGreen: "#6F8E72",
      borderYellow: "#E8C762"
    },
    fontFamily: {
      serif: ["Cormorant Garamond", "Georgia", "serif"],
      sans: ["Inter", "Arial", "sans-serif"],
      display: ["Bebas Neue", "Impact", "sans-serif"]
    },
    borderRadius: {
      xs: "6px",
      sm: "8px",
      md: "14px",
      lg: "18px",
      xl: "24px",
      pill: "999px"
    },
    boxShadow: {
      card: "0 12px 30px rgba(47, 81, 56, 0.12)",
      soft: "0 8px 22px rgba(31, 29, 26, 0.08)",
      hover: "0 16px 36px rgba(47, 81, 56, 0.16)"
    }
  }
}
```

---

# 24. Recommended Component Names

Use clear names so the codebase does not become a haunted junk drawer.

## Shared Components

```txt
SiteHeader
SiteFooter
Container
Section
EditorialHero
ImpactHero
DecorativeLineArt
PrimaryButton
SecondaryButton
TextCTA
TrustStrip
IconBadge
ImageCard
```

## Shop Components

```txt
CuratedCategoryGrid
CuratedCategoryCard
ProductCategoryGrid
ProductCategoryCard
HowItWorks
HowItWorksStep
CustomInquiryCTA
```

## Vinyl Product Components

```txt
VinylProductPage
SizeSelectionGrid
SizeSelectionCard
UploadArtworkSection
FileGuidelinesCard
RushProductionToggle
BeforeYouOrderStrip
ProjectGallery
```

---

# 25. Page Implementation Rules for Cursor / Antigravity

Use this as the main AI instruction when building or refactoring pages.

```txt
Build the website using the New Project Designs design system exactly.

Use:
- Cream backgrounds, not pure white.
- Deep sage green and warm yellow as the main palette.
- Cormorant Garamond for editorial headlines.
- Bebas Neue for the bold “Curated for Your Event” style and category card titles.
- Inter for navigation, body text, buttons, labels, and form text.
- Rounded cards, soft shadows, generous spacing, and image-first layouts.
- Thin botanical and geometric line art as subtle decoration.
- Warm event photography with consistent lighting and palette.

Do not:
- Add new colors.
- Add new fonts.
- Use dark gradients.
- Use gray dashboard-style form UI.
- Use heavy borders.
- Use bright saturated colors.
- Use generic ecommerce card layouts.
- Use pure white backgrounds unless absolutely required inside form inputs.
- Use random icons or multiple icon styles.
- Overcrowd sections.

All pages should feel curated, premium, event-focused, and custom-made.
```

---

# 26. Accessibility Rules

## Contrast

- Body text must stay readable on cream, yellow, and green backgrounds.
- Use `--color-text-primary` on light backgrounds.
- Use `--color-text-inverse` on dark green backgrounds.
- On green cards, yellow text is acceptable for large display text, but body text should be tested for readability.

## Buttons

- Buttons must have visible hover and focus states.
- Minimum clickable height should be 40px.
- Primary CTAs should be easy to identify.

## Images

- Every image needs meaningful alt text.
- Decorative line art should use empty alt text or be hidden from screen readers.
- Product thumbnails should describe the product and use case.

Example alt text:

```txt
Acrylic wedding sign on a wooden stand beside a glass vase with greenery.
Vinyl lettering being applied to a soft fabric backdrop.
Cream event wall with custom welcome vinyl lettering.
```

## Keyboard

- All cards that act as links must be keyboard focusable.
- Selected size cards must expose selected state.
- File upload must be reachable by keyboard.

---

# 27. Final QA Checklist

Before approving any page, check:

- Background is cream, not pure white.
- Typography hierarchy is clear.
- Hero title uses the correct font style.
- Green and yellow colors match this system.
- Cards have soft shadows and rounded corners.
- Images feel warm, styled, and cohesive.
- Forms do not feel like admin software.
- Decorative line art is subtle.
- CTAs are clear but not loud.
- Mobile layout stacks cleanly.
- All interactive elements have hover and focus states.
- Product pages feel premium, not like a generic checkout flow.
- The page still works without decorative art.
- No random colors or fonts were introduced.

---

# 28. Quick Page Mapping

## Curated for Your Event

Use:

- `ImpactHero`
- `CuratedCategoryGrid`
- `CuratedCategoryCard`
- `TrustStrip`

Fonts:

- Hero title: Bebas Neue
- Card titles: Bebas Neue
- Body: Inter

Colors:

- Background: Cream
- Cards: Green / Yellow / Green
- Footer strip: Deep green

---

## Signage & Print Shop

Use:

- `EditorialHero`
- `ProductCategoryGrid`
- `ProductCategoryCard`
- `HowItWorks`
- `CustomInquiryCTA`

Fonts:

- Hero title: Cormorant Garamond
- Card titles: Cormorant Garamond
- Body: Inter

Colors:

- Background: Cream
- Acrylic card: Cream
- Vinyl card: Soft yellow
- CTA strip: Deep green

---

## Vinyl Printing Product Page

Use:

- `EditorialHero`
- `SizeSelectionGrid`
- `SizeSelectionCard`
- `UploadArtworkSection`
- `FileGuidelinesCard`
- `RushProductionToggle`
- `BeforeYouOrderStrip`
- `ProjectGallery`
- `TrustStrip`

Fonts:

- Hero title: Cormorant Garamond
- Step titles: Cormorant Garamond
- Size labels: Cormorant Garamond
- UI text: Inter

Colors:

- Background: Cream
- Size card footer: Pale yellow
- Selected border: Deep green
- Upload border: Sage green
- Rush strip: Pale yellow
- Add to cart: Deep green
- Trust strip: Deep green

---

# 29. Non-Negotiables

These are not suggestions.

1. Do not use dark gradient cards.
2. Do not use gray ecommerce placeholders.
3. Do not use more than three font families.
4. Do not use pure white page backgrounds.
5. Do not mix random photography styles.
6. Do not make the product page feel like a form-first checkout.
7. Do not replace the yellow/green system with pastel wedding colors.
8. Do not overuse script fonts.
9. Do not let decorative line art compete with content.
10. Do not reduce card spacing to cram content.

The brand should feel like a curated event design studio that happens to sell products, not a shop that happens to have a logo.