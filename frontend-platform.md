# frontend-platform

This repository is the **central Nx monorepo for the entire CyberRangeCZ Platform frontend**. It consolidates all client-side applications and shared libraries, providing a cohesive, integrated, and efficiently managed user interface for the diverse functionalities of the CyberRangeCZ ecosystem. The migration of various previously standalone `frontend-*` repositories into this monorepo signifies a strategic move towards a unified frontend development approach.

## Key Features and Structure:

*   **Nx Monorepo Architecture**: Uses the Nx workspace tools to manage multiple interdependent applications and libraries within a single Git repository. This allows for better code sharing, consistent tooling, and simplified dependency management.
*   **Angular-based Development**: All components and applications within this monorepo are built using the Angular framework (TypeScript, HTML, CSS).
*   **Local Development Setup**: Provides clear instructions for running the frontend locally against a deployed CyberRangeCZ backend (e.g., using `devops-helm`). It highlights necessary Keycloak/OIDC configurations for development.
*   **Dockerized Deployment**: Includes a `Dockerfile` for building the frontend application into a Docker image, and a `push.sh` script to automate the deployment of this image to an existing Kubernetes environment managed by Helm.
*   **Applications (`apps` directory)**:
    *   `cyberrangecz-platform`: This is the main user-facing application for the CyberRangeCZ platform, providing the primary user interface and overall application shell.
    *   `cyberrangecz-platform-e2e`: Contains end-to-end tests for the main platform application, ensuring its functionality and user flows are working correctly.
*   **Shared Libraries (`libs` directory)**: The core of the monorepo, promoting code reuse and modularity:
    *   **`agenda`**: Libraries providing UI components for specific "agenda" views, such as `sandbox-agenda` (for managing sandbox schedules), `training-agenda` (for training schedules), and `user-and-group-agenda` (for user and group management interfaces).
    *   **`api`**: Client libraries that abstract away REST API calls to the various backend microservices. These include `api-common` for shared API utilities, and specific clients for `sandbox-api`, `training-api`, `user-and-group-api`, and `visualization-api`.
    *   **`model`**: Contains key TypeScript interface and class definitions for objects (Data Transfer Objects - DTOs) received from the backend APIs. This ensures type safety and consistency across the frontend when interacting with `sandbox-model`, `training-model`, `user-and-group-model`, and `visualization-model`.
    *   **`utils`**: A collection of small, reusable utility functions, classes, and services, covering aspects like shared UI `components`, `routing` utilities, and miscellaneous helper functions (`misc`).
    *   **`components`**: A general collection of self-contained, reusable UI components that can be shared across different applications or agendas.

## Role in CyberRangeCZ:

The `frontend-platform` repository is paramount to the CyberRangeCZ platform:

*   **Unified User Interface**: Provides the single, integrated web interface through which users (trainees, instructors, administrators) interact with all aspects of the CyberRangeCZ platform.
*   **Enhanced Developer Productivity**: The Nx monorepo structure, combined with shared libraries, significantly boosts developer productivity and ensures consistency in UI/UX across the platform.
*   **Centralized Frontend Logic**: Consolidates all frontend business logic, data fetching (via API clients), and state management.
*   **Integration Point**: Serves as the primary integration point with all backend microservices, orchestrating data display and user interactions.
*   **Scalable and Maintainable**: The modular design allows for independent development and testing of features while maintaining a coherent overall application.

This repository is the face of the CyberRangeCZ platform, providing the interactive and dynamic user experience that enables effective cybersecurity training and administration.
