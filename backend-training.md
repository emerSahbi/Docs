# backend-training

This repository contains the "CyberRangeCZ Platform Training" backend microservice, which serves as the **core management component for linear training exercises** within the CyberRangeCZ platform. It is a comprehensive, multi-module Java service responsible for defining, orchestrating, tracking, and auditing training sessions, integrating with various other platform services to provide a complete training environment.

## Key Technologies and Features:

*   **Java with Spring Boot**: Built using Java and the Spring Boot framework, providing a modular and scalable backend solution.
*   **Multi-Module Project**: Structured into several distinct Maven modules, each handling a specific layer or concern:
    *   **`training-rest`**: Implements the REST API endpoints for communication with the frontend, with Swagger for API documentation.
    *   **`training-api`**: Contains Data Transfer Object (DTO) classes, validation rules, Swagger annotations, and MapStruct mappers for efficient object conversion.
    *   **`training-service`**: Houses the core business logic, orchestrating interactions with the persistence layer, combining data, and communicating with other microservices.
    *   **`training-persistence`**: Manages data persistence using Spring Data JPA with Hibernate, backed by a PostgreSQL database. It utilizes QueryDSL for advanced data filtering.
    *   **`training-elasticsearch`**: Dedicated module for auditing and retrieving training-related data from Elasticsearch, including event classes that describe specific actions or occurrences.
*   **Secure API Access**: Requires OpenID Connect (OIDC) configuration for authentication and authorization, ensuring that interactions with the service are secure. It depends on an OIDC Provider and the `backend-user-and-group` service.
*   **Inter-service Communication**: Designed to call other microservices, indicating its role as an orchestrator in complex training workflows. Includes an environment variable for waiting on other service preconditions.
*   **Containerized Deployment**: Designed for deployment as a Docker container, with detailed instructions for building and running. It listens on port `8083`.
*   **API Documentation**: Provides comprehensive API documentation via Swagger UI, accessible locally once the service is running.
*   **Code Quality and Security**: Adheres to rigorous code quality and security standards, integrating tools like Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check.

## Role in CyberRangeCZ:

The `backend-training` service is central to the platform's ability to deliver structured training:

*   **Training Management**: Manages the lifecycle of linear training exercises, from definition and setup to execution and completion.
*   **Data Tracking**: Records trainee progress, performance metrics, and interactions, storing them in PostgreSQL for core data and in Elasticsearch for auditing and analytics.
*   **Integration Hub**: Acts as an integration point, coordinating between different microservices (e.g., user management, sandbox management, adaptive components) to provide a cohesive training experience.
*   **Frontend Data Provider**: Serves the necessary data and APIs for the `frontend-training-portal` and other frontend components to display training content, track progress, and facilitate user interaction.

This service is fundamental for defining, delivering, and evaluating the structured, linear cybersecurity training programs offered by the CyberRangeCZ platform.
