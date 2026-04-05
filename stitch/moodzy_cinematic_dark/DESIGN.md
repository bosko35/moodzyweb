# Design System: The Cinematic Immersive Framework

## 1. Overview & Creative North Star
**The Creative North Star: "The Neon Nocturne"**

This design system is engineered to move away from the static, "boxed-in" nature of traditional SaaS and towards a fluid, cinematic experience. It is designed for a mobile-native generation that values emotion over utility. We treat the interface not as a tool, but as a stage. 

By leveraging **intentional asymmetry**, we break the predictable rhythm of the scroll. Elements should overlap, typography should feel "loud," and the dark canvas should feel like an endless void where content—not the UI—is the star. This is "Editorial Futurism": high-contrast, prestigious, and deeply atmospheric.

---

## 2. Colors & Surface Philosophy
The palette is rooted in a "Deep Space" black, utilizing high-chroma accents to guide the eye through the dark.

### The Palette (Material Mapping)
*   **Background / Surface:** `#0e0e12` (The Void)
*   **Primary (Purple):** `#ba9eff` | **Primary Dim:** `#8455ef`
*   **Secondary (Pink):** `#ff6b9a` | **Secondary Dim:** `#ff6b9a`
*   **Tertiary (Cyan):** `#81ecff` | **Tertiary Dim:** `#00d4ec`
*   **Error:** `#ff6e84`

### The "No-Line" Rule
To maintain a premium, cinematic feel, **1px solid borders are strictly prohibited for sectioning.** We do not "box" content. Boundaries must be defined through:
1.  **Background Shifts:** Use `surface-container-low` vs. `surface-container-high`.
2.  **Shadow Depth:** Use light-diffusion rather than lines.
3.  **Negative Space:** Use the spacing scale to create mental boundaries.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of smoked glass. 
*   **Base:** `surface` (#0e0e12)
*   **Sectioning:** `surface-container-low` (#131318)
*   **Interactive Cards:** `surface-container-highest` (#25252c)
*   **The Glass Rule:** For floating overlays (players, navigation bars), use `rgba(255, 255, 255, 0.06)` with a `backdrop-blur` of 20px-40px.

---

## 3. Typography: The Editorial Voice
We use **Space Grotesk** for impact and **Inter** for legibility. Typography is our primary design element, not just a carrier of information.

*   **Display (Space Grotesk):** Large, aggressive, and cinematic. Use `display-lg` (3.5rem) for hero titles. Tighten letter-spacing (-2%) for a "premium poster" look.
*   **Headlines (Space Grotesk):** Use `headline-lg` (2rem) for section headers. Always use high-contrast `on-background` colors.
*   **Body (Inter):** Reserved for metadata and descriptions. Use `body-md` (0.875rem) to keep the UI feeling "pro" and less cluttered.
*   **Hierarchy Note:** Use color to drive importance. `on-surface` for primary headings, `on-surface-variant` for secondary metadata.

---

## 4. Elevation & Depth
In a dark UI, traditional shadows often disappear. We use **Tonal Layering** and **Luminescence** instead.

*   **The Layering Principle:** Stack `surface-container` tiers. A `surface-container-highest` card sitting on a `surface` background provides all the "lift" required.
*   **Ambient Glows:** Instead of black shadows, use a 4-8% opacity shadow tinted with the `primary` (purple) or `secondary` (pink) tokens. This mimics the glow of a screen in a dark room.
*   **The Ghost Border:** If a container requires a boundary (e.g., on top of a video feed), use a `0.5px` border of `outline-variant` at 20% opacity. It should be felt, not seen.
*   **Corner Radii:** Apply `xl` (3rem) for hero cards and `md` (1.5rem) for inner components. Never use sharp corners.

---

## 5. Components & Interaction

### Buttons (High-Impact CTAs)
*   **Primary:** A gradient transition from `primary` to `primary-dim`. No borders. `lg` (2rem) corner radius.
*   **Secondary:** Glassmorphism style. `surface-variant` at 40% opacity with a subtle `ghost border`.
*   **Interaction:** On hover/active, apply a subtle `primary` outer glow (8px blur).

### Cards & Vertical Feeds
*   **Forbid Dividers:** Use vertical white space (32px-48px) to separate content modules.
*   **Asymmetric Grids:** In a list of cards, vary the aspect ratios. Use a 9:16 card next to two 4:5 cards to create an editorial, magazine-style layout.

### Immersive Components
*   **The Mood-Blur:** Behind high-priority content, place a large, blurred vector shape (150px blur) using the `secondary` or `tertiary` tokens at 10% opacity. This creates an emotional "aura" around the content.
*   **Glass Navigation:** Bottom bars must be floating, not docked. Use `surface-container-highest` at 60% opacity with a heavy backdrop blur and `xl` (3rem) corner radius.

---

## 6. Do’s and Don'ts

### Do:
*   **Do** use extreme scale. Make headlines huge and metadata tiny to create "drama."
*   **Do** use "Breathing Room." High-end design requires more padding than you think (24px-32px gutters).
*   **Do** lean into the vertical. This is a mobile-first world; design for the thumb and the vertical scroll.

### Don’t:
*   **Don't** use pure white text (#FFFFFF). Use `on-background` (#f9f5fc) to prevent eye strain on dark backgrounds.
*   **Don't** use standard "SaaS Blue." Every accent must feel like a neon light or a cinematic filter.
*   **Don't** use 100% opaque borders. They kill the immersive, "infinite" feel of the dark UI.
*   **Don't** center-align everything. Use intentional left-alignment with asymmetric imagery to create movement.