# frontend-theme

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"CyberRangeCZ Platform Theme"**, an Angular library dedicated to unifying the visual styling, branding, and user experience across all frontend applications within the CyberRangeCZ platform. Its primary goal was to establish a consistent look and feel by centralizing styles, fonts, icons, and other static assets.

## Historical Functionality:

*   **Comprehensive Theming Solution**: Provided a complete set of design tokens and utility classes for consistent styling:
    *   **Color System**: Defined an extensive palette of CSS custom properties (variables) for primary, secondary, tertiary, neutral, and error colors, each with multiple shades, along with utility classes (`bg-*`, `fg-*`) for easy application.
    *   **Layout Utilities**: Included utility classes for Flexbox (`vertical-flex`, `horizontal-flex`, `jc-*`, `ai-*`) to streamline responsive and consistent layouts.
    *   **Sizing and Spacing**: Offered utility classes for setting dimensions (`w-*`, `h-*`) and applying uniform gaps, padding, and margins (`g-*`, `p-*`, `m-*`).
    *   **Visual Enhancements**: Provided custom scrollbar styling (`round-scrollbar`), resizer highlighting (`highlighted-resizer`), and predefined CSS animations (`fadeIn`, `slideDown`, etc.) to enrich the user interface.
*   **Centralized Assets**: Managed common assets like logos and icons, providing a standardized way to include them in any frontend application.
*   **Modular Styles**: Allowed for importing a complete theme (`apply-all.scss`) or individual style modules for more granular control.
*   **Angular Integration**: Designed as an Angular library, making it easy to integrate into other Angular projects via npm.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **Sass/SCSS**: For defining and organizing the styles and color variables.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, the `frontend-theme` repository was indispensable for ensuring a cohesive and professional brand identity across the CyberRangeCZ platform. It provided:

*   **Consistent UI/UX**: Guaranteed that all frontend applications shared a uniform visual language, improving user familiarity and reducing cognitive load.
*   **Accelerated Development**: Enabled frontend developers to build new features quickly by leveraging a rich set of predefined styles and components, without needing to recreate basic styling from scratch.
*   **Brand Enforcement**: Ensured that the platform's visual identity was consistently applied throughout all user-facing interfaces.

Its integration into the `frontend-platform` monorepo represents a strategic consolidation of frontend development, centralizing all shared styling and assets into a single, cohesive codebase. This approach enhances maintainability, simplifies updates, and reinforces the platform's unified user experience.
