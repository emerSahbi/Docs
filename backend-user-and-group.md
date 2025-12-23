# backend-user-and-group

This repository contains the "CyberRangeCZ Platform User and Group" backend microservice, which is the **central Identity and Access Management (IAM) system** for the entire CyberRangeCZ platform. Its fundamental role is to manage users, groups, and roles, providing authentication, authorization, and a structured permissions framework for all other services and users within the platform.

## Key Technologies and Features:

*   **Java with Spring Boot**: Built using Java and the Spring Boot framework, providing a robust, scalable, and secure foundation for IAM.
*   **Layered Architecture**: Organized into distinct modules for clear separation of concerns:
    *   `.api`: Defines DTOs and mappers for consistent data exchange.
    *   `.definition`: Contains framework configurations, Swagger annotations, and exception handling.
    *   `.persistence`: Manages database interactions, including entities, enums, and repositories.
    *   `.rest`: Implements the RESTful API endpoints for external communication.
    *   `.security`: **This is a core module, handling all aspects of authentication and authorization, including configuration of the identity provider, server security, and security logic, along with security object models.**
    *   `.service`: Implements the main business logic for user and group management.
*   **OpenID Connect (OIDC) Integration**: Fully integrated with an OIDC provider for user authentication, ensuring modern, secure, and standardized login procedures.
*   **Role-Based Access Control (RBAC)**: Manages roles and permissions for users, allowing for fine-grained control over what actions users and microservices can perform within the platform. It supports defining initial roles and users via `initial-users.yaml`.
*   **API Documentation**: Exposes a comprehensive RESTful API, with interactive documentation available via Swagger UI at `http://localhost:8084/swagger-ui.html`.
*   **Data Persistence**: Uses a PostgreSQL database for storing user, group, and role information, with support for in-memory H2 for development.
*   **Microservice Interoperability**: Serves as a foundational dependency for other services (e.g., `backend-security-commons`, `backend-training`, `backend-elasticsearch-service`), providing the necessary context for user identity and permissions.
*   **Containerized Deployment**: Designed for deployment as a Docker container, running on port `8084`.
*   **High Code Quality**: Adheres to the platform's rigorous standards for code quality and security, integrating tools like Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check.

## Role in CyberRangeCZ:

The `backend-user-and-group` service is critically important for the CyberRangeCZ platform because it:

*   **Enables Secure Multi-User Access**: Provides the infrastructure for managing multiple users, each with specific roles and permissions, essential for a training platform.
*   **Centralized Authentication and Authorization**: Acts as the single source of truth for user identities and their access rights, simplifying security management across the entire microservice ecosystem.
*   **Integrates with OIDC**: Connects the platform to external identity providers, allowing for flexible user onboarding and authentication.
*   **Supports RBAC**: Ensures that users only have access to the resources and functionalities appropriate for their roles (e.g., trainee, instructor, administrator).
*   **Foundational Service**: Many other services rely on `backend-user-and-group` to verify user identities and permissions before granting access to resources or performing actions.

This service is the cornerstone of secure and managed access within the CyberRangeCZ training environment, ensuring that users can interact with the platform safely and effectively according to their designated roles.
