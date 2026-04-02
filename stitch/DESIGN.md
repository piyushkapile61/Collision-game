```markdown
# Design System Strategy: The Squishy Playground

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"Tactile Joy: The High-Fidelity Toybox."** 

We are moving away from the "flat" cartoon aesthetic of the last decade and leaning into a hyper-tactile, 3D-inspired editorial layout. Think of the UI not as a digital screen, but as a physical tray filled with chunky play-dough, molded plastic, and jelly-filled shapes. 

To break the "standard template" look, we employ **Intentional Asymmetry.** Elements should rarely feel perfectly centered or static; instead, use the `Spacing Scale` to create "weighted" layouts where headers might lean left while primary CTAs float with a slight rotational offset. We treat the screen as a gravity-filled space where elements have "heft" and "squish."

---

## 2. Colors: The Primary Playground
This palette is rooted in high-contrast energy, utilizing a specialized Material Design mapping to ensure "The Squishy Playground" feels premium rather than cheap.

### The "No-Line" Rule (Sectioning)
Standard 1px lines are strictly forbidden. To separate content, use **Tonal Blocking.** Use the `surface-container` tiers to create "puddles" of color. A card should be defined by its shift from `surface` (#eeffdd) to `surface-container-low` (#d9ffbd), not by a stroke.

### Surface Hierarchy & Nesting
Treat the UI as a series of molded plastic layers:
- **Base Layer:** `surface` (#eeffdd).
- **Secondary Puddles:** `surface-container` (#c2ff99) for grouping related content.
- **Interactive High Points:** `surface-container-highest` (#80ff2c) for the most interactive zones.

### Signature Textures & The "Plastic Glow"
To achieve the "Toy" look, do not use flat fills for large areas. Apply a subtle **inner glow** (using `on-primary-container` at 20% opacity) to the top edge of buttons to simulate overhead lighting on a rounded plastic surface. For backgrounds, use a faint `outline-variant` (#d2c6a1) polka-dot pattern at 5% opacity to add depth.

---

## 3. Typography: Bubbly Authority
We utilize a hierarchy that balances playful character with editorial legibility.

*   **Display & Headlines (Plus Jakarta Sans):** These are our "Hero" fonts. Use `display-lg` (3.5rem) with a tight letter-spacing (-0.02em) to make headers feel like they are "squeezed" together. These should always be bold and feel heavy, like thick marker strokes.
*   **Titles & Body (Be Vietnam Pro):** This font provides the structural balance. While the headers are bubbly, the body copy remains clean and highly legible to ensure game mechanics are understood.
*   **The Signature Scale:** Use a "Size Jump" technique. A `display-lg` header should sit immediately next to a `body-md` description. This extreme contrast creates a "Big Toy/Small Instruction" aesthetic that feels custom and high-end.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "digital." We use **Ambient Blobs.**

*   **The Layering Principle:** Instead of shadows, stack `surface-container-lowest` (#ffffff) on top of `surface-container` (#c2ff99). The color shift provides the "lift."
*   **Ambient Shadows:** For floating elements (like modals), use a "Blobby Shadow": `on-surface` (#092100) at 6% opacity with a `40px` blur and a `12px` vertical offset. It should look like a soft shadow cast on a carpet, not a sharp digital drop.
*   **The "Ghost Border" Fallback:** If you must define a boundary on a complex background, use a "Marker Stroke": `outline` (#807757) at 15% opacity with a `3px` width. Avoid thin, high-contrast lines at all costs.

---

## 5. Components: Molded Primitives

### Buttons (The Jelly Beans)
*   **Primary:** Uses `primary` (#705d00) with `on-primary` (#ffffff) text.
*   **Shape:** `rounded-full` (9999px).
*   **Effect:** Add a 4px bottom "lip" using a darker shade (`on-primary-container`) to make the button look like a physical 3D block. 
*   **Animation:** On hover, the button should "squish" (scale-y: 0.9, scale-x: 1.1). On click, it "bounces" (scale: 0.95).

### Cards (The Trays)
*   **Style:** No borders. Use `surface-container-low` (#d9ffbd) with a `rounded-xl` (3rem) corner radius.
*   **Content:** Use `Spacing Scale 6` (2rem) for internal padding to give elements plenty of "breathing room" to bounce.

### Input Fields (The Carved Slots)
*   **Style:** Instead of a floating box, inputs should look "carved" into the surface. Use a slightly darker background (`surface-dim`) and an inner shadow to create a concave effect.

### Interaction Chips
*   **Style:** High-contrast `secondary-container` (#c6e7ff) with `rounded-md` corners. These should look like small plastic tabs or stickers stuck onto the UI.

---

## 6. Do’s and Don’ts

### Do:
*   **DO** use "Wumbo" Spacing. Give every element more room than you think it needs.
*   **DO** tilt icons or chips by 2-3 degrees randomly to create a "scattered toys" feel.
*   **DO** use the `tertiary` (#b42800) palette for "Danger" or "Critical" actions—it looks like "Cherry Red" candy.

### Don’t:
*   **DON'T** use 1px borders or sharp 90-degree corners. If it can poke an eye out, it doesn't belong in this system.
*   **DON'T** use pure black (#000000) for shadows or text. Always use `on-surface` (#092100) to keep the "ink" feeling soft.
*   **DON'T** use standard linear easing. Every transition must use a `cubic-bezier(0.34, 1.56, 0.64, 1)` "back-out" curve to create the signature "bounce."

---

## 7. Signature Component: The "Squish-Bar"
For progress bars or health meters, do not use a flat fill. Use a series of `rounded-full` segments that "pulse" slightly in size. As the bar fills, the new segments should "pop" into existence with a scale-up animation, looking like bubbles blowing up.