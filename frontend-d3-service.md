# frontend-d3-service

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"CyberRangeCZ Platform D3 Service"**, an Angular library designed to enhance the developer experience when working with D3.js (Data-Driven Documents) in Angular environments. It served as a wrapper, standardizing the import and usage of D3.js and its TypeScript typings across various frontend visualization components within the CyberRangeCZ platform.

## Historical Functionality:

*   **D3.js Wrapper**: Provided a convenient `D3Service` that could be injected into Angular components and services. This service would return the D3.js object, allowing developers to leverage D3's powerful data visualization capabilities without directly managing its imports and typings in every component.
*   **Improved Developer Experience**: Simplified the integration of D3.js into Angular projects, making it easier for developers to create complex and interactive data visualizations.
*   **Standardization**: Ensured a consistent approach to using D3.js across different frontend visualization modules within the platform.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **D3.js**: A JavaScript library for producing dynamic, interactive data visualizations in web browsers.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, the `frontend-d3-service` library was fundamental for the development of the many data visualization components within the CyberRangeCZ platform (e.g., clustering visualization, command visualizations). It provided:

*   **A Foundation for Visualizations**: Acted as a core utility for building all D3.js-based visualizations, ensuring consistency and reusability of the D3.js integration logic.
*   **Accelerated Development**: Allowed developers to focus on the visualization logic itself rather than the boilerplate of D3.js setup within Angular.

Its integration into the `frontend-platform` monorepo represents a strategic consolidation of frontend assets, centralizing common utilities and components to improve overall development efficiency and maintainability for the platform's user interfaces.
