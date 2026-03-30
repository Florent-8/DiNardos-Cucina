# Design System: The Artisanal Digital Mercato

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Archivist"**

This design system rejects the "fast-food" digital template in favor of a curated, editorial experience that mirrors the tactility of a high-end Italian neighborhood market. We are not building a generic e-commerce site; we are creating a digital extension of DiNardo’s Cucina & Mercato—a place that feels as if it were hand-pressed onto heavy linen paper. 

To achieve this, the system breaks the traditional rigid grid through **intentional asymmetry**. Hero elements should feel layered, like ingredients on a chef’s counter. We use exaggerated typography scales to create an editorial rhythm, where large, elegant serifs overlap subtle background textures, creating a sense of depth and heritage that "flat" design cannot replicate.

---

## 2. Colors & Tonal Depth
The palette is rooted in the earth: deep Mediterranean teals, sun-baked terracotta, and the warm ivory of fresh mozzarella.

### The "No-Line" Rule
Sectioning must never be achieved through 1px solid black or grey borders. Instead, boundaries are defined by **Background Color Shifts**. 
- Use `surface-container-low` (#f7f3ed) for secondary content sections sitting on the `background` (#fdf9f3).
- Content modules are separated by generous vertical white space (using the `20` or `24` spacing tokens) rather than structural lines.

### Surface Hierarchy & Nesting
Think of the UI as physical layers of parchment. 
*   **Level 0 (Base):** `surface` (#fdf9f3) - The primary canvas.
*   **Level 1 (Sections):** `surface-container-low` (#f7f3ed) - Sub-navigation or background cards.
*   **Level 2 (In-focus):** `surface-container-highest` (#e6e2dc) - High-priority callouts or flyouts.

### The "Glass & Gradient" Rule
To add soul to the interface, avoid purely flat shapes. 
- **CTAs:** Use a subtle linear gradient from `primary` (#006161) to `primary-container` (#2a7a7a) at a 45-degree angle to give buttons a "pressed ink" richness.
- **Overlays:** For navigation menus or filters, use `surface` with an 85% opacity and a `24px` backdrop-blur to create a "frosted glass" effect that allows the warm cream background to bleed through.

---

## 3. Typography
The typographic pairing is a conversation between the old world (Newsreader) and the modern utility (Work Sans).

*   **Display & Headlines (Newsreader):** Use these for "Brand Moments." Titles should be set with tight letter-spacing (-0.02em) to feel like a vintage Italian newspaper. Do not be afraid of `display-lg` (3.5rem); it is the "hero" of our page.
*   **Body & Labels (Work Sans):** Functional and clear. Body copy should always use `on-surface-variant` (#3f4948) for a softer, charcoal-grey read that is easier on the eyes than pure black.
*   **The Signature Style:** For high-end callouts (e.g., "Handmade Daily"), use `title-md` in **Italic Serif**, utilizing the `secondary` terracotta (#9d4311) color to act as a warm "stamp" of quality.

---

## 4. Elevation & Depth
In this design system, we do not use "drop shadows" in the traditional sense. We use **Tonal Layering**.

*   **The Layering Principle:** To lift a card, place a `surface-container-lowest` (#ffffff) card on a `surface-container` (#f1ede7) background. The change in "temperature" creates the lift.
*   **Ambient Shadows:** If a floating element (like a shopping cart drawer) requires a shadow, use a large `48px` blur with only 5% opacity. The shadow color must be a tinted `surface-dim` (#dddad4), never pure black.
*   **The "Ghost Border":** If a border is required for accessibility, use `outline-variant` (#bec9c8) at 20% opacity. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary-container` (#2a7a7a) with `on-primary` (#ffffff) text. Use `md` (0.375rem) roundedness—never fully rounded pill shapes.
*   **Secondary:** No fill. A "Ghost Border" of `primary` at 30% opacity.
*   **Tertiary:** Text-only in `secondary` (#9d4311) with an underline that only appears on hover.

### Cards (The "Mercato" Card)
*   **Style:** No borders. Background: `surface-container-low`. 
*   **Spacing:** Use `padding: 4` (1.4rem) to give product imagery room to breathe.
*   **Transition:** On hover, the background shifts to `surface-container-high` (#ebe8e2) and the image should subtly scale (1.02x).

### Input Fields
*   **Style:** Minimalist. Only a bottom border using `outline-variant`.
*   **Focus State:** The bottom border transforms into a `primary` (#006161) `2px` line. Labels should use `label-md` in `tertiary` (#63553a).

### Specialty Component: The "Deli Divider"
Instead of a horizontal rule, use a `tertiary-fixed-dim` (#d8c4a2) thin line that spans only 60% of the container width, centered, to signify a break in the "menu."

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts. Place a large image on the left and offset the text to the right using `spacing-12`.
*   **Do** treat white space as an active ingredient. If a section feels crowded, double the spacing.
*   **Do** use the `secondary` terracotta (#9d4311) sparingly for "Action" items like "Add to Basket" or "Special Offer" tags.

### Don't
*   **Don't** use pure black (#000000). Use `on-surface` (#1c1c18) for text.
*   **Don't** use "Pill" shapes for buttons. It feels too modern/tech. Stick to `md` or `lg` corner radii.
*   **Don't** use standard Material Design shadows. They break the "organic paper" feel of the market.
*   **Don't** use icons that are too "tech-heavy." Prefer thin-stroke, hand-drawn, or minimal serif-based iconography.

---

## 7. Spacing & Rhythm
Rhythm is achieved through the **1.7rem (Spacing 5)** base unit. 
*   Vertical gaps between sections: `16` (5.5rem) or `20` (7rem).
*   Internal component padding: `3` (1rem) or `4` (1.4rem).
*   Avoid "tight" layouts. DiNardo’s is an experience to be savored, not a task to be rushed.