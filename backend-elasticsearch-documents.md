# backend-elasticsearch-documents

This repository contains `crczp-elasticsearch-documents`, a Java library that defines the common data structures (Java classes) used for **event logging and data storage within Elasticsearch** across the CyberRangeCZ platform. Its primary purpose is to provide a standardized schema for documents that will be indexed and queried in Elasticsearch, ensuring consistency and ease of integration for various backend services.

## Key Technologies and Features:

*   **Java Library**: It is a standalone Java library (not a Spring Boot application), intended to be included as a dependency in other Java projects.
*   **Event Logging Focus**: The description in `pom.xml` clarifies its role in "Backend handling events logging via elasticsearch," indicating that the document definitions are specifically tailored for various types of events occurring within the CyberRangeCZ ecosystem.
*   **Standardized Document Schemas**: Provides a centralized location for defining the Java classes that represent the structure of documents (e.g., logs, metrics, activity records) stored in Elasticsearch. This consistency is crucial for effective data management and analysis.
*   **JSON Serialization/Deserialization**: Leverages `Jackson Annotations` to facilitate the seamless conversion of Java objects to JSON (for indexing in Elasticsearch) and from JSON back to Java objects (for retrieval).
*   **API Documentation Support**: Includes `Swagger Annotations`, suggesting that these document classes are often used as Data Transfer Objects (DTOs) in RESTful APIs. This allows for automatic generation of API documentation, describing the structure of data sent to and received from Elasticsearch-backed endpoints.
*   **Boilerplate Reduction**: Uses `Lombok` to minimize verbose code, making the document definitions cleaner and easier to maintain.
*   **Publishing to Maven Repository**: Configured for publishing to a Maven repository (like Maven Central), making it readily available for other CyberRangeCZ Java projects to consume as a dependency.
*   **High Code Quality**: Adheres to the platform's rigorous code quality and security standards, integrating tools such as Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check during the build process.

## Role in CyberRangeCZ:

The `backend-elasticsearch-documents` library is essential for:

*   **Data Consistency**: Ensures that all services interacting with Elasticsearch use a unified and consistent data model, preventing schema discrepancies and simplifying data interpretation.
*   **Centralized Logging and Analytics**: Underpins the platform's ability to collect, store, and analyze various events, logs, and metrics from training scenarios in a structured manner. This data is critical for monitoring, assessment, and post-exercise analysis.
*   **Streamlined Integration**: Simplifies the development process for new services that need to interact with Elasticsearch by providing ready-to-use data models.

By standardizing Elasticsearch document structures, this library enhances the overall observability, analytical capabilities, and maintainability of the CyberRangeCZ platform.
