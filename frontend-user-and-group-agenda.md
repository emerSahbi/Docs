# frontend-user-and-group-agenda

This repository contains an Angular library that provides the user interface components and services for managing users, groups, and microservices within the CyberRangeCZ platform. It serves as the frontend for the `backend-user-and-group` service. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-user-and-group-agenda` library is a collection of feature-specific modules that can be imported into a host application to provide user and group management capabilities.

The main features are:

*   **User Management**: A set of components and services for managing users.
    *   `user-overview`: A component to display a list of all users.
    *   `user-detail`: A component to show the details of a specific user.

*   **Group Management**: A set of components and services for managing groups.
    *   `group-overview`: A component to display a list of all groups.
    *   `group-detail`: A component to show the details of a specific group, including its members.
    *   `group-edit`: A component for creating and editing groups.

*   **Microservice Management**: A set of components and services for managing microservices and their roles.
    *   `microservice-overview`: A component to display a list of all registered microservices.
    *   `microservice-registration`: A component for registering a new microservice.

*   **Extensibility**: The library is designed to be extensible. Consuming applications can override the default navigation, error handling, and notification services by providing their own implementations.

## Role in CyberRangeCZ:

The `frontend-user-and-group-agenda` library provides the user interface for all user and group management tasks in the CyberRangeCZ platform. It is used by administrators to:

*   Manage the user base of the platform.
*   Create and manage groups of users.
*   Manage the registration and roles of microservices.

By providing a consistent and reusable set of components, this library simplifies the development of the main frontend application and ensures a consistent user experience for all user and group management tasks.
