# backend-answers-storage

This repository contains the "CyberRangeCZ Platform Answers Storage" backend microservice. Its primary role is to provide persistent storage and a programmatic interface (API) for managing "sandbox answers." These answers are typically dynamically generated configurations, solutions, or specific data points related to individual training sandboxes, which are pushed to this service by components like `backend-ansible-runner`.

## Key Technologies and Features:

*   **Java with Spring Boot**: Developed using Java and the Spring Boot framework, providing a scalable and maintainable microservice.
*   **Persistent Data Storage**:
    *   **Spring Data JPA**: Manages data persistence, allowing for interaction with relational databases.
    *   **PostgreSQL**: The preferred production database, indicated by its runtime dependency.
    *   **H2 Database**: An in-memory database used for development and testing environments.
    *   **Flyway**: Utilized for managing database schema migrations, ensuring consistency and versioning of the database structure.
*   **RESTful API**: Exposes a RESTful API at `/answers-storage/api/v1`, allowing other services within the CyberRangeCZ platform to store, retrieve, and potentially delete sandbox answers. API documentation is generated using Swagger/Springfox.
*   **Advanced Querying**: Integrates **QueryDSL** for building type-safe and sophisticated database queries, suggesting that the service supports complex retrieval mechanisms for the stored answers.
*   **Object Mapping**: Uses **MapStruct** for efficient and type-safe mapping between different data transfer objects and entities.
*   **Internal Dependencies**: May rely on internal/proprietary Maven repositories for shared libraries, as indicated by the `repositories` section in `pom.xml`.
*   **Code Quality and Security**: Adheres to the platform's high standards for code quality and security, incorporating tools like Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check.
*   **Containerization**: Includes a `Dockerfile` for easy deployment as a Docker container.

## Role in CyberRangeCZ:

The `backend-answers-storage` service is crucial for several aspects of the CyberRangeCZ platform:

*   **Centralized Answer Repository**: Serves as a reliable, central repository for all dynamically generated sandbox-specific information.
*   **Enabling Dynamic Content**: Allows for the creation of unique training scenarios where certain "answers" (e.g., vulnerabilities, flags, user credentials) are unique to each sandbox, preventing trainees from sharing solutions directly.
*   **Facilitating Assessment and Feedback**: Other services can query this storage to compare trainee actions against the expected answers, providing automated assessment and feedback.
*   **Decoupling Services**: Decouples the process of answer generation (e.g., `backend-ansible-runner`) from the consumption of these answers, promoting a modular microservice architecture.

By providing a robust and accessible storage for sandbox-specific data, this service significantly enhances the dynamism and effectiveness of the CyberRangeCZ training environments.
