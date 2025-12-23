# frontend-sandbox-model

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"CyberRangeCZ Platform Sandbox Model"**, an Angular (TypeScript) library dedicated to defining the **frontend data models (interfaces and classes) for sandbox-related entities**. Its primary purpose was to provide a standardized, type-safe representation of data exchanged with the `backend-sandbox-service`, ensuring consistency and clarity across all frontend components that display, manipulate, or interact with sandbox information.

## Historical Functionality:

*   **Data Model Definition**: Defined TypeScript interfaces and classes for key sandbox entities, such as `SandboxDefinition`, `SandboxInstance`, `SandboxPool`, `SandboxAllocation`, and related attributes.
*   **Type Safety**: Ensured that frontend components working with sandbox data had a clear and consistent understanding of the data's structure, reducing runtime errors and improving code quality.
*   **Consistency with Backend**: These models served as the frontend counterpart to the Data Transfer Objects (DTOs) defined in the `backend-sandbox-service`, facilitating seamless communication and mapping between the frontend and backend.
*   **Reusability**: Allowed other frontend libraries and applications to import and use these models, preventing redundant data model definitions across the monorepo.

## Technologies Used:

*   **Angular / TypeScript**: Leveraging TypeScript's strong typing features to define clear data structures.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, the `frontend-sandbox-model` library was fundamental for the modularity, maintainability, and reliability of the CyberRangeCZ frontend:

*   **Foundation for API Clients**: Provided the types that `frontend-sandbox-api` would use to define its service contracts.
*   **UI Development**: Guided UI components in displaying sandbox information correctly and consistently.
*   **Reduced Development Errors**: Minimized potential errors arising from mismatches between expected and received data structures.

Its integration into the `frontend-platform` monorepo signifies a consolidation of all frontend data model libraries into a single `libs/model` structure. This centralizes the platform's understanding of its core data entities, enhancing overall development efficiency and maintainability.
