# Design System Document: CDM Pajarero

## 1. Overview & Creative North Star: "The Kinetic Editorial"
This design system is built to move. It rejects the static, boxy nature of traditional web templates in favor of a high-velocity, editorial aesthetic. Our Creative North Star is **"The Kinetic Editorial"**—a visual language that mirrors the grit of mountain biking and the explosive energy of trail running. 

We break the "template" look by utilizing intentional asymmetry, high-contrast typographic scales, and layered depth. Instead of centering everything, we use offset layouts and overlapping elements to create a sense of forward motion. This is not a flat interface; it is a tactical, multi-layered environment designed for the outdoors.

---

## 2. Colors
Our palette is rooted in high-visibility "safety" tones and deep, obsidian-like neutrals, creating a professional, high-performance atmosphere.

### The Color Logic
*   **Primary (`#44b8f8`):** The "Atmospheric Blue." Use this for key actions and navigational anchors.
*   **Secondary (`#e0ed1d`):** The "High-Vis Yellow." This is our energy injector. Use it for high-impact CTAs and essential highlights.
*   **Neutral Foundation:** We rely on `surface` (`#0e0e0e`) and `surface-container` tiers to build weight.

### Strategic Application Rules
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for defining sections. Boundaries must be defined solely through background color shifts (e.g., a `surface-container-low` section sitting against a `surface` background).
*   **Surface Hierarchy & Nesting:** Treat the UI as a series of physical layers. Use `surface-container-lowest` for the most recessed areas and `surface-container-highest` for prominent interactive cards. This creates "nested" depth that feels structural rather than decorated.
*   **The "Glass & Gradient" Rule:** Floating elements (like navigation bars or hovering stat cards) should utilize Glassmorphism. Use semi-transparent surface colors with a `backdrop-blur` effect. 
*   **Signature Textures:** For Hero backgrounds and Primary CTAs, use a subtle linear gradient transitioning from `primary` (`#44b8f8`) to `primary-container` (`#30aaea`) at a 135-degree angle. This adds a "machined" finish that flat hex codes cannot achieve.

---

## 3. Typography
The typography is the engine of this design system. We use a high-contrast pairing to balance technical precision with aggressive energy.

*   **Display & Headlines (Space Grotesk):** This is our "Technical Bold." It feels engineered and modern. Use `display-lg` (3.5rem) and `headline-lg` (2rem) for high-impact editorial statements. Headlines should often be italicized or set in All-Caps to reinforce the sense of speed.
*   **Body & Titles (Lexend):** This is our "Legibility Anchor." Lexend was designed to reduce visual noise. Use `body-lg` (1rem) for long-form content and `title-md` (1.125rem) for UI labels.
*   **Visual Hierarchy:** Use wide tracking (letter-spacing) for `label-sm` to create a premium, "spec-sheet" feel on technical data points like race times or elevations.

---

## 4. Elevation & Depth
In this design system, elevation is an environmental property, not a drop-shadow effect.

*   **The Layering Principle:** Stacking tiers is the primary way to show importance. A `surface-container-lowest` card placed on a `surface-container-low` background creates a soft, natural lift.
*   **Ambient Shadows:** If a "floating" effect is required (e.g., a modal or a primary button), shadows must be extra-diffused. Use a blur value of 24px-48px with an opacity of 6% or 8%. The shadow color should be a tinted version of the `on-surface` color to mimic natural ambient light.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, it must be a "Ghost Border." Use the `outline-variant` token at 15% opacity. Never use 100% opaque borders.
*   **Glassmorphism:** Apply a 12px-20px backdrop blur to semi-transparent surface layers. This allows the background imagery of trails and mountains to bleed through, integrating the UI into the environment.

---

## 5. Components

### Buttons (The Kinetic Triggers)
*   **Primary:** Background: `secondary` (`#e0ed1d`), Text: `on-secondary` (`#505600`). Use `round-md` (0.375rem). The hover state should include a subtle 4px vertical "lift" and an ambient shadow.
*   **Secondary:** Background: `surface-variant`, Text: `primary`. No border.
*   **Tertiary:** Text-only with an underline that only spans 60% of the text width, using the `secondary` color for a custom editorial look.

### Cards & Lists
*   **Constraint:** Forbid the use of divider lines.
*   **Separation:** Use `spacing-8` (2.75rem) to separate list items or use alternating background shifts between `surface-container-low` and `surface-container-lowest`.
*   **Image Integration:** Images within cards should use a slight zoom-on-hover effect to maintain the "Kinetic" feel.

### Specialized Sports Components
*   **Race Stats Chip:** Use `surface-container-highest` with `label-md` typography. These should feel like "tactical stickers" placed on the UI.
*   **The Elevation Profile:** A custom component using a `primary` to `primary-dim` gradient fill, placed on a `surface-container-lowest` track. Avoid axes; use floating labels for a cleaner look.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** lean into asymmetry. Off-center your headlines to the left while pushing body text to a right-aligned column.
*   **Do** use the `secondary` (yellow) color sparingly as a "strike" of energy—think of it as a highlighter, not a paint bucket.
*   **Do** use large amounts of `spacing-16` or `spacing-20` between major sections to let the high-impact typography breathe.

### Don’t:
*   **Don’t** use standard "Card" containers with 1px borders and heavy shadows. It breaks the high-end editorial feel.
*   **Don’t** use center-alignment for long-form text. It feels too "blog-standard" and loses the aggressive, technical edge.
*   **Don’t** mix more than two `surface-container` levels in a single nested group, or the interface will begin to look cluttered and "muddy."
*   **Don’t** use default black for shadows. Always tint your shadows with a hint of the background hue to maintain tonal depth.