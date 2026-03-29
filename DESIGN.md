# Design System Documentation: The Sensory Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Sensory Editorial."**

This system rejects the sterile, "app-like" feel of generic recipe platforms. Instead, it draws inspiration from high-end, heavy-stock culinary magazines and independent lifestyle journals. We are creating a digital environment that feels as tactile and warm as a sun-drenched kitchen. To achieve this, we move away from rigid, boxed-in grids and embrace **intentional asymmetry, expansive breathing room, and tonal layering.**

By prioritizing sophisticated typography scales and organic color transitions over traditional UI borders, we create an experience that feels curated rather than programmed. Every screen should feel like a composed photograph, where the UI supports the "aroma" of the content.

---

## 2. Colors
Our palette is a sophisticated interplay between the heat of the hearth (Terracotta) and the coolness of the garden (Sage).

### Tonal Foundation
- **Primary (`#9a4024`):** The "Terracotta" heart. Used for primary actions and moments of heat.
- **Secondary (`#4e644e`):** The "Sage" balance. Used for health-focused elements, herb-related tags, or soothing secondary interactions.
- **Surface (`#faf9f6`):** Our "Creamy Off-White" canvas. This is a warm neutral that prevents the "blue-light" fatigue of pure white.

### The "No-Line" Rule
Standard 1px borders are strictly prohibited for sectioning. We define space through volume, not lines.
- **Boundary Definition:** Use background color shifts. A `surface-container-low` (`#f4f3f1`) section should sit against a `surface` (`#faf9f6`) background to indicate a change in context.
- **Surface Hierarchy & Nesting:** Treat the UI as stacked sheets of fine paper. An inner card should use `surface-container-lowest` (`#ffffff`) to "lift" off a `surface-container` (`#efeeeb`) background.

### The "Glass & Gradient" Rule
To add soul to the interface, use subtle, non-linear gradients.
- **Signature Textures:** For main Hero backgrounds or large CTAs, transition from `primary` (`#9a4024`) to `primary-container` (`#ba5839`).
- **Glassmorphism:** Floating navigation bars or recipe-timer overlays must use a 60% opacity of `surface` with a `24px` backdrop blur. This allows the vibrant food photography to "bleed" through, creating a deep, integrated feel.

---

## 3. Typography
We use a high-contrast typographic pairing to bridge the gap between tradition and modern utility.

- **The Voice (Headings):** **Noto Serif.** This font carries the heritage of printed cookbooks. Use `display-lg` (`3.5rem`) for recipe titles to create an editorial impact that feels authoritative and inviting.
- **The Engine (Instructions):** **Manrope.** A highly legible, modern sans-serif. Used for the "work" of the app—ingredients and steps. Its geometric nature provides a clean counterpoint to the organic serif.

**Hierarchy Strategy:**
- **Asymmetry:** Align `headline-lg` to the left with a wider-than-usual margin (Spacing `8`) while the body copy follows a narrower column. This creates "white space with purpose."
- **Tonal Contrast:** Use `on-surface-variant` (`#56423d`) for secondary labels to soften the visual noise and keep the focus on the primary `on-surface` (`#1a1c1a`) headlines.

---

## 4. Elevation & Depth
Elevation is achieved through **light and tint**, never through heavy shadows.

- **The Layering Principle:** Depth is created by "stacking" surface tiers.
    - *Base:* `surface`
    - *Mid-Ground:* `surface-container-low`
    - *Foreground:* `surface-container-lowest` (Cards)
- **Ambient Shadows:** When an element must float (e.g., a "Start Cooking" FAB), use a shadow with a `32px` blur, 4% opacity, tinted with the `on-surface` color (`#1a1c1a`). It should feel like a soft glow of light, not a drop shadow.
- **The "Ghost Border" Fallback:** If a border is required for accessibility (e.g., in input fields), use the `outline-variant` (`#dcc1b9`) at **15% opacity**. This creates a "suggestion" of a container without breaking the editorial flow.

---

## 5. Components

### Buttons
- **Primary:** `primary` (`#9a4024`) fill with `on-primary` (`#ffffff`) text. Use `rounded-full` for a friendly, organic feel. Apply a subtle gradient transition to `primary-container`.
- **Secondary:** `secondary-container` (`#cee6cb`) fill with `on-secondary-container` (`#526853`) text. No border.

### Cards & Recipe Feeds
- **Style:** Forbid dividers. Separate cards using Spacing `6` or `8`.
- **Image Treatment:** Use `rounded-xl` (`1.5rem`) for all food photography to echo the "soft" brand personality.

### Input Fields & Search
- **Style:** Use `surface-container-highest` (`#e3e2e0`) for the input background with a "Ghost Border."
- **Focus State:** Transit`ion the ghost border to a 100% opaque `primary` line, but only at the bottom (2px), mimicking a high-end stationery aesthetic.
``
### Selection Elements (Ch`ips & Checkboxes)
- **Chips:** Use `tertiary`-container` (`#7e7362`) for unselected states. Selected states should pop with `secondary` (`#4e644e`).
- **Checkboxes:** For recipe ingredient lists, use a custom "Circle-Check" rather than a square. When checked, the item text should transition to `on-surface-variant` with a simple strikethrough.

### Editorial Special: The "Step" Component
For the cooking mode, use a full-screen `surface` background. The step number should be a large, 10% opacity `display-lg` Noto Serif digit in the background, with the `body-lg` instruction text floating elegantly over it.

---

## 6. Do's and Don'ts

### Do:
- **Do** use generous white space. If a layout feels "crowded," double the spacing between the image and the title.
- **Do** use the Spacing Scale religiously. Consistent gaps of `1.4rem` (4) and `2.75rem` (8) create a rhythmic, professional "grid-less" feel.
- **Do** mix font weights. Use `title-md` in Bold for ingredient amounts and Regular for the ingredient names.

### Don't:
- **Don't** use pure black (`#000000`) or pure grey. Always use the provided `on-surface` and `outline` tokens, which are "warmed" by the terracotta and sage tones.
- **Don't** use 1px solid dividers. If you need to separate content, use a `surface-container` fill or a Spacing `8` vertical gap.
- **Don't** use "Default" rounded corners. Stick to `md` (`0.75rem`) for small elements and `xl` (`1.5rem`) for large cards to maintain the "approachable" feel.

### COLOR PALLETTE:
- `#000000` `#3A0A00` `#5F1600` `#7E2C11` `#9D4226` `#BD5A3B` `#DD7352` `#FD8C69` `#FFB59F` `#FFDBD1` `#FFEDE8` `#FFFFFF`
- `#000000` `#0C200F` `#213523` `#374C38` `#4E644E` `#667D66` `#80977F` `#9AB198` `#B5CDB3` `#D1E9CE` `#DFF7DC` `#FFFFFF`
- `#000000` `#221A0E` `#382F22` `#4F4537` `#675D4D` `#817565` `#9B8F7D` `#B7A997` `#D3C4B1` `#F0E0CC` `#FEEFDA` `#FFFFFF`
- `#000000` `#1A1C1A` `#2F312F` `#464745` `#5E5F5D` `#777775` `#91918E` `#ABABA9` `#C7C6C4` `#E3E2E0` `#F1F1EE` `#FFFFFF`