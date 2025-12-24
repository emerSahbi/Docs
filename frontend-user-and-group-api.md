# frontend-user-and-group-api

This repository contains an Angular library that provides a set of services for interacting with the `backend-user-and-group` microservice in the CyberRangeCZ platform. It serves as the API layer for the user and group management frontend. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-user-and-group-api` library abstracts the communication with the backend into a set of strongly-typed and reusable services.

*   **API Service Layer**: The library defines a set of abstract service classes, each corresponding to a specific backend resource. These services define the contract for all user and group management API communications. The key services include:
    *   `UserApiService`: For managing users.
    *   `GroupApiService`: For managing groups.
    *   `MicroserviceApiService`: For managing microservice registrations.
    *   `RoleApiService`: For managing roles.

*   **Data Mapping**: The library is responsible for mapping the Data Transfer Objects (DTOs) from the backend to the frontend's internal data model (provided by `@crczp/user-and-group-model`).

*   **Extensibility**: The library provides default implementations for the API services, but consuming applications can provide their own custom implementations through Angular's dependency injection mechanism.

## Role in CyberRangeCZ:

The `frontend-user-and-group-api` library is a crucial component of the frontend architecture. It provides:

*   **A clean and consistent API**: For all user and group management operations.
*   **Decoupling**: It decouples the frontend components from the backend APIs.
*   **Type Safety**: It provides type safety for all API communications.

In summary, this library provides a standardized and extensible way for the frontend to communicate with the `backend-user-and-group` service.
