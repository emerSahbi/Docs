# backend-elasticsearch-service

This repository contains the "CyberRangeCZ Platform Elasticsearch Service," a backend microservice whose primary function is to provide a structured and secure API for **retrieving and interacting with documents stored in an Elasticsearch instance**. It acts as an intermediary, abstracting the complexities of direct Elasticsearch queries and offering a higher-level interface for other frontend and backend components of the CyberRangeCZ platform.

## Key Technologies and Features:

*   **Java with Spring Boot**: Built using Java and the Spring Boot framework, providing a robust and scalable foundation for a microservice architecture.
*   **Layered Architecture**: The project is modularly divided into distinct layers:
    *   `rest`: Implements the REST API endpoints for external communication (with frontends and other microservices), documented using Swagger.
    *   `service`: Contains the core business logic, orchestrating calls to the `data` layer and combining results. It also manages transactions and AOP (Aspect-Oriented Programming) concerns.
    *   `data`: Handles the low-level interactions with Elasticsearch, utilizing the Elasticsearch `RestHighLevelClient` for efficient data retrieval.
    *   `api`: Defines Data Transfer Object (DTO) classes, including validation rules and Swagger annotations, ensuring consistent data contracts across the platform. MapStruct is used for efficient object mapping.
*   **Secure API Access**: Requires OpenID Connect (OIDC) configuration for authentication and authorization, ensuring that only authorized entities can access the Elasticsearch data. It also depends on the `backend-user-and-group` service for user context.
*   **Integration with `backend-elasticsearch-documents`**: Implicitly uses the document definitions provided by `backend-elasticsearch-documents` to ensure type-safety and consistency when working with Elasticsearch data.
*   **Containerized Deployment**: Designed for deployment as a Docker container, making it easily manageable and scalable within the platform's Kubernetes environment. It listens on port `8085`.
*   **Code Quality and Security**: Adheres to the platform's high standards for code quality and security, integrating tools like Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check in its build process.

## Role in CyberRangeCZ:

The `backend-elasticsearch-service` is a central piece of the platform's observability and analytics infrastructure:

*   **Centralized Data Access**: Provides a unified and controlled gateway for all services to access the rich event and log data stored in Elasticsearch.
*   **Abstracts Elasticsearch Complexity**: Hides the intricacies of Elasticsearch queries and data structures, allowing developers of other services to interact with Elasticsearch data using simpler, higher-level API calls.
*   **Enables Analytics and Monitoring**: Supports frontend components (e.g., visualization dashboards) in querying and displaying critical information derived from training activities, system events, and security logs.
*   **Security Integration**: Enforces access control to sensitive log and event data via OIDC, ensuring data privacy and integrity.

By providing a robust, secure, and structured interface to Elasticsearch, this service significantly enhances the analytical capabilities and overall operational visibility of the CyberRangeCZ platform.
