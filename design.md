# New Project Designs - Design System

This document outlines the core design language, typography, color palette, and styling rules extracted from the `index.html` landing page.

## 1. Typography

The design relies on a carefully selected typography pair to convey an elegant, premium, and structured look.

*   **Serif (Elegant & Classic):** `"Cormorant Garamond", Georgia, serif`
    *   *Usage:* Branding, logos, secondary elegant headings.
*   **Display (Bold & Impactful):** `"Bebas Neue", Impact, sans-serif`
    *   *Usage:* Large hero headlines, uppercase card titles. Usually paired with slight letter spacing (`tracking-[0.01em]`).
*   **Sans-Serif (Clean & Readable):** `"Inter", Arial, sans-serif`
    *   *Usage:* Body text, navigation links, overlines, and UI buttons.

## 2. Color Palette

The color scheme is natural, earthy, and warm, focusing on rich greens and soft creams.

### Backgrounds & Surfaces
*   **Cream (Primary Background):** `#F7F3EA` - Used as the main body background.
*   **Cream Soft:** `#FBF8F0`
*   **Card Cream:** `#F9F4E8`

### Brand Greens (Primary Accents)
*   **Green 900 (Darkest):** `#2F5138`
*   **Green 800 (Primary UI/Buttons):** `#3F6848` - Used for primary buttons, footer, and text selection background.
*   **Green 700 (Cards & Large Text):** `#4E7654`
*   **Green 600:** `#5F8763`

### Accent Yellows (Secondary Accents)
*   **Yellow 700:** `#B89632`
*   **Yellow 600:** `#D7B94E`
*   **Yellow 500 (Highlights & Badges):** `#F3D36D`
*   **Yellow 400:** `#F7DA81`
*   **Yellow 200:** `#F9E7B5`
*   **Yellow Soft:** `#FFF1C8`

### Typography Colors
*   **Text Primary (Headings & Dark Text):** `#1F1D1A`
*   **Text Secondary (Body Text):** `#4F5A4D`
*   **Text Muted (Subtle Text):** `#6D716A`
*   **Text Inverse (Text on Dark Backgrounds):** `#FBF8F0`

### Borders
*   **Border Light:** `#DDD5C6`
*   **Border Green:** `#6F8E72`
*   **Border Yellow:** `#E8C762`

## 3. UI Elements & Styling

### Shadows & Depth
*   **Card Shadow:** `0 12px 30px rgba(47, 81, 56, 0.12)`
*   **Soft Shadow:** `0 8px 22px rgba(31, 29, 26, 0.08)`
*   **Hover Shadow (Elevated state):** `0 16px 36px rgba(47, 81, 56, 0.16)`

### Border Radii
*   **Extra Small:** `6px`
*   **Small:** `8px`
*   **Medium:** `14px`
*   **Large:** `18px`
*   **Extra Large:** `24px`
*   **Pill (Buttons):** `999px`

### Global CSS Details
*   **Text Selection:** Selected text uses `#3F6848` (Green 800) background with `#FBF8F0` text.
*   **Custom Scrollbar:** The scrollbar is slim (6px), with a `#F7F3EA` track and a `#3F6848` (Green 800) thumb, giving it a seamless, integrated feel.

## 4. Interaction Patterns

*   **Buttons / Links:** Primary actions use `bg-green800` with pill shapes. Hover states trigger an opacity reduction (`hover:opacity-80`) rather than a color change.
*   **Cards:** Interactive cards use a smooth upward translation (`hover:-translate-y-[3px]`), swap to the stronger `shadow-hover`, and scale their inner images slightly (`group-hover:scale-105`) over a 700ms duration for a premium feel.
*   **Overlines:** Section markers (like "SHOP EVENT DETAILS") use `font-sans`, uppercase formatting, `text-[14px]`, bold weight, and very wide letter spacing (`tracking-[0.18em]`).
