# frontend-training-portal

This repository contains the main frontend application for the CyberRangeCZ platform, serving as the primary entry point for users to interact with the training, sandbox, and user management features. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-training-portal` is a full-featured Angular application that integrates various frontend libraries into a cohesive user experience.

*   **Application Shell**: It provides the main application shell, including the overall layout, navigation, and menu structure. It acts as a container for all the other frontend features.

*   **Integration of Feature Modules ("Agendas")**: The portal's primary role is to integrate the various "agenda" libraries, which contain the UI components for specific domains:
    *   `@crczp/training-agenda`: For managing the entire lifecycle of training exercises.
    *   `@crczp/sandbox-agenda`: For managing sandbox environments.
    *   `@crczp/user-and-group-agenda`: For managing users and groups.

*   **Routing and Navigation**: It defines the main routing configuration for the application, using lazy loading to on-demand load the different feature modules. This improves the application's performance by only loading the code that is needed for the user's current task.

*   **Authentication and Authorization**: The portal is responsible for handling user authentication and authorization.
    *   It integrates with an OAuth2/OIDC identity provider to log users in.
    *   It uses a robust system of route guards to enforce role-based access control (RBAC), ensuring that users can only access the features that are appropriate for their role (e.g., `TrainingDesigner`, `TrainingOrganizer`, `Trainee`).

*   **Global Services**: It provides a set of global services that are used throughout the application, such as:
    *   **HTTP Interceptors**: For handling common HTTP tasks like error logging, showing loading indicators, and refreshing authentication tokens.
    *   **Notification and Error Handling**: For providing a consistent way to display notifications and handle errors.

*   **Deployment**: The presence of a `Dockerfile` indicates that the portal is designed to be built and deployed as a standalone containerized application.

## Role in CyberRangeCZ:

The `frontend-training-portal` is the face of the CyberRangeCZ platform. It is the single web application that all users interact with, whether they are designing training, managing sandboxes, or taking a training course. It brings together all the disparate frontend features into a unified and seamless experience.
