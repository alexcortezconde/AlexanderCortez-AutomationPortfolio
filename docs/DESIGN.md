# Design System Document: The Kinetic Engineer

## 1. Overview & Creative North Star
**Creative North Star: "The Neural Architect"**
This design system moves away from the static, box-heavy layouts of traditional engineering portfolios. It embraces a "Neural Architect" aesthetic—where the precision of RPA (Robotic Process Automation) meets the fluid, organic intelligence of AI. 

To break the "template" look, we employ **Intentional Asymmetry**. Components should not always align to a rigid 12-column grid; instead, use overlapping elements and high-contrast typography scales to create a sense of movement. The UI should feel like a living terminal: high-tech, clean, and deeply layered.

## 2. Colors & Surface Philosophy
The palette is rooted in `Ink Black` and `Deep Blue`, providing a sophisticated foundation for high-energy accents.

### The Color Logic
- **Primary (`#a5cbea` / `primary-container: #003049`):** Represents the "Logic Layer." Use this for core structural elements and primary actions.
- **Secondary (`#8fd1de` / `secondary-container: #005662`):** The "Flow Layer." Represents the Stormy Teal of automation processes.
- **Tertiary (`#ffb689` / `tertiary-container: #4c2100`):** The "Human Element." Use Harvest Orange and Brandy tones sparingly for high-impact callouts or error-handling that feels intentional, not alarming.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Physical boundaries are an artifact of old web design. In this system, boundaries are defined by:
1.  **Tonal Shifts:** Transitioning from `surface` (#001524) to `surface-container-low` (#071d2d).
2.  **Glassmorphism:** Using semi-transparent surfaces with a `backdrop-blur` of 12px–20px to create separation.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked "Frosted Logic Gates."
- **Base Level:** `surface` (#001524).
- **In-Page Sections:** `surface-container-low` (#071d2d).
- **Interactive Cards:** `surface-container-high` (#172c3c) or `surface-container-highest` (#233747).
*Nesting Example:* A `surface-container-highest` code snippet box sitting inside a `surface-container-low` project description.

### Signature Textures
Avoid flat backgrounds. Use a subtle linear gradient for Hero sections: `surface` to `primary-container` at a 135-degree angle. This adds "soul" and depth to the "Deep Blue" foundation.

## 3. Typography
We pair the technical precision of **Inter** with the architectural character of **Space Grotesk**.

- **Display & Headlines (Space Grotesk):** These are your "Statement" layers. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to convey authority. Headline scales should feel "oversized" compared to standard web defaults.
- **Body & Labels (Inter):** The "Execution" layer. Inter provides maximum readability for technical documentation and code explanations. 
- **The Contrast Play:** Pair a `display-sm` headline in `on-surface` with a `label-md` uppercase sub-header in `tertiary` (#ffb689). This high-contrast pairing (large/geometric vs. small/functional) is the hallmark of high-end editorial design.

## 4. Elevation & Depth
Depth is a functional tool, not just an aesthetic choice. It represents the "Layers of Logic" in an AI system.

### The Layering Principle
Achieve lift through color, not just shadow. 
- **Tonal Layering:** A card using `surface-container-lowest` placed on a `surface` background creates a "sunken" or "embedded" feel—perfect for input fields or code blocks.

### Ambient Shadows
When an element must "float" (e.g., a mobile navigation bar or a hovered project card):
- **Shadow:** Use `on-surface` at 6% opacity.
- **Blur:** 40px to 60px.
- **Spread:** -10px (to keep the shadow "tucked" and clean).

### Glassmorphism & Ghost Borders
For floating interactive panels, use a semi-transparent `surface-bright` (#273b4c) at 60% opacity with a `backdrop-filter: blur(16px)`. 
- **The Ghost Border:** If a stroke is required, use `outline-variant` (#42474d) at **15% opacity**. This creates a "shimmer" effect on the edge without creating a hard visual stop.

## 5. Components

### Buttons (The Interaction Points)
- **Primary:** Gradient fill from `primary` to `secondary`. No border. Roundedness: `md` (0.375rem).
- **Tertiary (Ghost):** No background. Text in `primary`. On hover, a `surface-container-high` background fades in.
- **Interactive State:** On click, use a subtle `0.98` scale transform to simulate a physical "press."

### Cards (Project & Skill Modules)
- **Styling:** No dividers. Separate content using the Spacing Scale (e.g., `spacing-6` between header and body).
- **Background:** `surface-container-low`.
- **Hover:** Shift to `surface-container-high` and apply the "Ghost Border" at 20% opacity.

### Inputs (Code Aesthetic)
- **Text Fields:** Use `surface-container-lowest`. The label should use `label-sm` in `primary` (#a5cbea), positioned strictly above the field, never floating inside.
- **Focus State:** Instead of a thick border, use a 1px `primary` bottom-border only, mimicking a terminal cursor.

### Specialized Component: The "Logic Terminal"
A custom container for code snippets or RPA workflows.
- **Background:** `surface-container-lowest` (#00101c).
- **Detail:** A top-bar using `surface-container-highest` with three `0.5rem` circles (Papaya Whip, Harvest Orange, Brandy) to mimic a window interface.

## 6. Do's and Don'ts

### Do
- **Do** use `spacing-16` and `spacing-20` for vertical breathing room between major sections.
- **Do** use "Papaya Whip" (`#ffecd1`) for tiny, high-contrast details like icon accents or bullet points.
- **Do** use smooth CSS transitions (300ms, cubic-bezier(0.4, 0, 0.2, 1)) for all hover states.

### Don't
- **Don't** use 100% black (`#000000`). Always use `Ink Black` (#001524) to maintain depth and color harmony.
- **Don't** use standard "drop shadows" (e.g., black with 25% opacity). It muddies the Deep Blue palette.
- **Don't** use "Harvest Orange" for large background areas. It is an accent intended to draw the eye to specific data points or CTAs.
- **Don't** use dividers or lines to separate list items. Use `spacing-4` padding and subtle `surface` color shifts.