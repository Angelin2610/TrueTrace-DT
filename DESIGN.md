# Design System Document: The Ethical Editorial

## 1. Overview & Creative North Star
**The Creative North Star: "The Living Ledger"**

Traditional sustainability apps often feel either overly clinical or distractingly "earthy." This design system rejects both extremes in favor of a **High-End Editorial** approach. We are not just displaying data; we are publishing a manifesto of transparency. 

The "Living Ledger" aesthetic moves beyond the grid-bound "template" look. It utilizes **intentional asymmetry**, **balanced negative space**, and **tonal layering** to create a digital experience that feels as prestigious and trustworthy as a premium broadsheet. We replace rigid containers with clear, readable layouts where information is separated by color hierarchy rather than lines.

---

## 2. Colors
Our palette is a sophisticated interplay of deep forest greens and ethereal sages, grounded by a "Paper-White" foundation.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Boundaries must be established through color shifts. A `surface-container-low` section sitting on a `surface` background is the only way to denote a change in content area. 

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—stacked sheets of fine, translucent paper.
- **Base Layer:** `surface` (#f8faf8)
- **Secondary Sectioning:** `surface-container-low` (#f2f4f2) 
- **Interactive Cards:** `surface-container-lowest` (#ffffff) for maximum "lift" against the background.
- **Deep Nesting:** Use `surface-container-high` (#e6e9e7) for inset elements like search bars or code blocks.

### The "Glass & Gradient" Rule
To elevate the "TrueTrace" brand, use **Glassmorphism** for floating navigation bars or modal headers. 
- **Effect:** Background Blur (20px) + `surface` at 70% opacity.
- **Signature Texture:** Use a subtle linear gradient from `primary` (#1b4332) to a lighter tonal variant for high-impact CTAs to provide a "velvet" depth that flat color cannot replicate.

---

## 3. Typography
We utilize **Plus Jakarta Sans** to provide a contemporary, editorial feel with excellent legibility across all device sizes.

*   **Display (lg/md/sm):** Used for "Hero" impact data—like a sustainability score. Use `primary` color and tight letter spacing (-0.02em).
*   **Headline & Title:** These are your "Editorial Anchors." Use `headline-md` for section titles to establish clear, authoritative hierarchy.
*   **Body (lg/md):** Our primary storytelling tool. Ensure line-height is comfortable (1.4x - 1.5x) to maintain a clean and modern aesthetic.
*   **Label:** Used for data visualization legends and metadata. Use `on-surface-variant` to keep these secondary to the main narrative.

---

## 4. Elevation & Depth
We eschew traditional "material" shadows in favor of **Tonal Layering** and moderate corner softening.

*   **The Layering Principle:** Depth is achieved by "stacking" tokens. A `surface-container-lowest` card placed on a `surface-container` background creates a soft, natural lift.
*   **Ambient Shadows:** For floating action buttons or high-priority modals, use a "Botanical Shadow": 
    *   `X: 0, Y: 8, Blur: 24, Spread: -2`
    *   Color: `on-surface` at **4% to 6% opacity**. 
*   **Roundedness:** Components feature **moderate roundedness** (Level 2), providing a professional yet approachable feel that bridges the gap between sharp architectural lines and organic shapes.

---

## 5. Components

### Buttons
*   **Primary:** `primary` background with `on-primary` text. Use **medium-radius** corners. No border.
*   **Secondary:** `surface-container-highest` background. Subtle, tonal, and sophisticated.
*   **Tertiary:** No background. `primary` text weight set to "Medium."

### Cards & Lists
*   **Strict Rule:** No dividers. Use **standardized vertical white space** (Level 2) to separate list items, ensuring a rhythmic, clean flow.
*   **Traceability Cards:** Use a `surface-container-low` background with moderate corner radii. Use the `primary-fixed` token for "Verified" badges.

### Data Visualization (The "Trace" Elements)
*   **Progress Bars:** Use a `surface-variant` track with a `primary` fill.
*   **Impact Icons:** Keep icons "Line-Weight Light" (1.5px stroke). Never use solid, heavy icons.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use moderate roundedness for all container elements to maintain a cohesive, modern visual language.
*   **Do** lean heavily on `surface-container` shifts to group related sustainability metrics.
*   **Do** use standard padding and margins (Level 2) to ensure clarity without excessive whitespace.

### Don't:
*   **Don't** use pure black (#000000). Always use `on-surface`.
*   **Don't** use sharp, 0px corners; maintain the established moderate roundedness for brand consistency.
*   **Don't** use drop shadows on text or buttons. Let the color contrast and tonal shifts do the work.
*   **Don't** over-compress the layout; keep the "Normal" spacing to ensure the editorial feel isn't lost to density.