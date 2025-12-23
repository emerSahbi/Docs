# frontend-sandbox-api

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"CyberRangeCZ Platform Sandbox API"**, an Angular client library specifically designed to facilitate communication between frontend applications and the `backend-sandbox-service`. Its primary role was to abstract the complexities of making HTTP requests and handling data from the backend, providing a clean and type-safe interface for frontend components to manage sandbox-related resources.

## Historical Functionality:

*   **Backend Service Client**: Provided a set of Angular services that acted as clients for the REST API exposed by the `backend-sandbox-service`.
*   **DTO to Model Mapping**: Included default implementations for mapping Data Transfer Objects (DTOs) received from the backend to internal frontend models. These internal models were imported from the `frontend-sandbox-model` repository, ensuring consistency between the frontend's understanding of sandbox data and the backend's.
*   **Abstraction Layer**: Shielded other frontend components from direct knowledge of the backend API's structure, URLs, and data formats, allowing them to interact with sandbox data through simple service calls.
*   **Extensibility**: Designed to be extensible, allowing developers to override default API service implementations by extending abstract classes, providing flexibility for custom logic or mock data during development.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **TypeScript**: Ensures type-safety for API interactions.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, the `frontend-sandbox-api` library was essential for the modularity and maintainability of the CyberRangeCZ frontend:

*   **Decoupling Frontend and Backend**: Promoted a clean separation of concerns between the user interface and the backend logic, making both layers easier to develop, test, and maintain independently.
*   **Consistent API Interaction**: Ensured a standardized way for all frontend components to interact with sandbox management functionalities.
*   **Accelerated Development**: Allowed frontend developers to quickly build UI features related to sandboxes without getting bogged down in low-level HTTP client code.

Its integration into the `frontend-platform` monorepo signifies a consolidation of all frontend API client libraries, providing a single, coherent `libs/api` structure for managing all backend communications. This enhances maintainability and centralizes the interaction logic for the entire frontend application.
