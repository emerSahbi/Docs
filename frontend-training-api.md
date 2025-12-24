# frontend-training-api

This repository contains an Angular library that provides a set of services for interacting with the `backend-training` and related microservices in the CyberRangeCZ platform. It acts as a bridge between the frontend components and the backend APIs. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The primary role of the `frontend-training-api` library is to abstract the communication with the backend into a set of strongly-typed and reusable services.

*   **API Service Layer**: The library defines a set of abstract service classes, each corresponding to a specific backend resource. These services define the contract for all training-related API communications. The key services include:
    *   `TrainingDefinitionApi`: For managing training definitions.
    *   `TrainingInstanceApi`: For managing training instances.
    *   `TrainingRunApi`: For managing training runs.
    *   `AdaptiveDefinitionApi`, `AdaptiveInstanceApi`, `AdaptiveRunApi`: For managing adaptive training scenarios.
    *   `UserApi`: For user-related operations.
    *   `TrainingEventApi`: For handling events within a training.
    *   `VisualizationApi`: For fetching data for visualizations.
    *   `MitreTechniquesApi`: For interacting with MITRE ATT&CK data.
    *   `CheatingDetectionApi` and `DetectionEventApi`: For managing cheating detection.

*   **Data Mapping**: The library is responsible for mapping the Data Transfer Objects (DTOs) from the backend to the frontend's internal data model (provided by `@crczp/training-model`). This separation of concerns makes the frontend more resilient to changes in the backend API.

*   **Extensibility**: The library is designed to be extensible. While it provides default implementations for the API services, consuming applications can provide their own custom implementations through Angular's dependency injection mechanism. This is useful for mocking the backend during testing or for adding custom logic to the API calls.

## Role in CyberRangeCZ:

The `frontend-training-api` library is a critical part of the frontend architecture of the CyberRangeCZ platform. It provides:

*   **A Single Source of Truth**: For all training-related API interactions.
*   **Decoupling**: It decouples the frontend components from the backend APIs, which makes the code easier to maintain and test.
*   **Type Safety**: By using TypeScript classes and interfaces, it provides type safety for all API communications, reducing the likelihood of runtime errors.

In summary, this library provides a clean, consistent, and extensible way for the frontend to communicate with the backend training services.
