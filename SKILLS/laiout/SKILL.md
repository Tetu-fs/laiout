---
name: laiout
description: A UI layout skill that minimizes visual decoration and structures layouts so they are easy for humans to style later.
---

# UI Layout Skill

## Purpose

The AI is responsible for UI layout and the placement of information and existing components, not visual design or decoration.

The UI should be structured so that humans can freely add and adjust visual design later.

## Basic Rules

1. Do not add visual decoration unless explicitly requested by the user.
2. Use existing UI elements, styles, and components as they are.
3. Do not create new UI elements or styles that duplicate or closely resemble existing ones.
4. Follow the layout principles described below.
5. Do not modify, override, or neutralize the existing visual design unless explicitly requested.
6. Do not make design decisions beyond what is necessary to implement the layout.

### For Modern Web Frontend Projects

When implementing styles, follow the CSS framework or styling approach already used by the project.

If the project uses a specific CSS framework or styling method, follow it rather than introducing a different approach.

## Layout Principles

1. **Proximity**

   Place closely related elements near each other.

2. **Alignment**

   Align elements using consistent reference lines such as edges, centers, or baselines.

3. **Repetition**

   Use consistent structures and layout methods for elements with the same role.

4. **Hierarchy**

   Group elements according to their relationships.

   Use more spacing between groups than between elements within a group.

5. **Whitespace**

   Provide sufficient whitespace so that elements do not feel crowded.

6. **Reading Order**

   Keep the DOM order and visual reading order aligned whenever possible.

## Spacing

- Use the defined spacing scale for `margin`, `padding`, `gap`, and similar spacing properties.
  - Base values: `4 / 8 / 12 / 16 / 24 / 32 / 48 / 64px`
  - This spacing scale applies only to spacing such as `margin`, `padding`, and `gap`. Do not force it onto element widths, heights, font sizes, or other dimensions.
- Use `4px` for fine spacing around icons and other small elements.
- Use smaller spacing for more closely related elements.
- Use larger spacing between separate groups.
- Prefer `gap` over `margin` for spacing between sibling elements.

## Responsive Layout

- Use mobile-first layout by default, with approximately `414px` as a reference viewport width.
  - For dashboards and other information-dense management interfaces, PC-first is acceptable unless otherwise specified.
- Do not unnecessarily shrink elements on smaller screens. Reflow or reposition elements when necessary.
- Existing UI conventions and explicit user requirements take precedence.

### Viewport Width Breakpoints

- Mobile: `414px` or less
- Tablet: `1024px` or less
- PC: greater than `1024px`

## Positioning

- Prefer Normal Flow, Flexbox, and Grid for layout.
- Unless there is a genuine layout reason, do not use absolute positioning or transforms to manually adjust element positions.
  - This does not apply to UI elements that inherently require positioning, such as overlays or overlapping elements.
- Do not add unnecessary wrapper elements.
- Place important information and primary actions where they can be naturally discovered according to the reading and interaction order.

## Visual Design

- Do not introduce new visual design decisions unless explicitly requested.
- Preserve and reuse existing visual styles when using existing UI elements.
- Existing colors, backgrounds, borders, shadows, gradients, typography, and other visual styles should remain effective.
- Do not override or neutralize existing styles.
- For typography, follow explicit user requirements or existing UI styles.

## Project-specific Rules

<!-- Add project-specific rules here, such as components, icons, CSS frameworks, -->
<!-- styling conventions, design systems, or other project-specific requirements. -->
