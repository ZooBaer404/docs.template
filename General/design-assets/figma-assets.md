<!--
START OF: figma-assets.md
Purpose: Centralized documentation for Figma files, usage guidelines, and access instructions.
Update Frequency: Whenever design files are updated or new ones are added.
Location: docs/design-assets/figma-assets.md
-->

# Figma Assets

This document contains information about our Figma-based design assets, including links, naming conventions, and best practices for collaboration.

---

## Figma Project Links

| Name           | Description                                       | Link                                                                |
|----------------|---------------------------------------------------|---------------------------------------------------------------------|
| Main UI Kit    | Core components, buttons, forms, typography, etc. | [Open in Figma](https://www.figma.com/file/your-ui-kit-link)        |
| Design System  | Tokens, grids, breakpoints, and guidelines.       | [Open in Figma](https://www.figma.com/file/your-design-system-link) |
| Mobile Mockups | Screens and flows for mobile interfaces.          | [Open in Figma](https://www.figma.com/file/your-mobile-link)        |
| Web Mockups    | Screens and user flows for desktop/web.           | [Open in Figma](https://www.figma.com/file/your-web-link)           |

> Make sure you are signed in with your org email to access restricted files.

---

## Naming Convention

- **Prefix pages** with their platform: `WEB -`, `MOBILE -`, `COMPONENTS -`
- **Frame titles** must match feature or route names (e.g. `Login`, `Dashboard > Admin`, `Settings > Notifications`)
- Use `/` in component names for nesting: `Button/Primary`, `Card/Product`

---

## Collaboration Guidelines

- Never edit **Main Components** without syncing with the design lead.
- Use the **Comment mode** for all feedback unless you're assigned a design task.
- **Duplicate pages** for experiments (use prefix `WIP - YourName`).
- Always keep **version history clean** — publish changes with meaningful descriptions.

---

## Tips for Developers

- Use the **Inspect** tab in Figma for pixel-perfect values.
- Export assets in SVG or WebP when possible.
- Match design tokens with what's defined in `/styles/` or `/theme/`.

---

## Versioning

Design tokens and UI components follow semver-style tags:
- `v1.0.0` — Initial release
- `v1.1.0` — New components added
- `v1.1.1` — Minor updates or fixes

Version tags are tracked inside `README` of the UI Kit file.

---

## Access Issues?

If you cannot open or edit files:
1. Ping a team lead in the `#design-infra` Slack channel.
2. Or, request access via Figma (please include your org email).

---

<!-- END OF: figma-assets.md -->
