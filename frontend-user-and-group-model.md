# frontend-user-and-group-model

This repository contains an Angular library that defines the data model for all user and group management features in the CyberRangeCZ platform. It serves as the single source of truth for the data structures used across the user and group management frontend. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-user-and-group-model` library provides a set of TypeScript classes and interfaces that represent the data structures for the user and group management lifecycle.

The data model is organized into the following categories:

*   **Core Entities**:
    *   `User`: Represents a user in the platform.
    *   `Group`: Represents a group of users.
    *   `Microservice`: Represents a registered microservice.

*   **Role Management**:
    *   `UserRole`: Represents a role assigned to a user.
    *   `MicroserviceRole`: Represents a role that is specific to a microservice.

## Role in CyberRangeCZ:

The `frontend-user-and-group-model` library is a fundamental component of the frontend architecture. It ensures that all other frontend libraries are using the same data structures, which provides:

*   **Consistency**: It eliminates data-related conflicts and inconsistencies between different parts of the application.
*   **Type Safety**: By using TypeScript, it provides strong type checking at compile time, which reduces the number of bugs.
*   **Maintainability**: By centralizing the data model, it makes the code easier to understand, maintain, and evolve.

In essence, this library provides the data model that the rest of the user and group management frontend uses to communicate and operate.
