# backend-guacamole

This repository contains the `guacamole-service` backend microservice, which plays a pivotal role in enabling secure and authenticated remote access to sandbox environments within the CyberRangeCZ platform via Apache Guacamole. Its primary function is to act as an intermediary, facilitating WebSocket connections to `guacd` (the Guacamole daemon) instances running in individual sandboxes, and providing additional "Quality of Life" features for users.

## Key Technologies and Features:

*   **Java with Spring Boot**: Developed using Java with a modern Spring Boot 3.x framework, making it a robust and scalable microservice.
*   **WebSocket Gateway**: Designed to establish and manage WebSocket connections to `guacd` instances, which handle the actual streaming of remote desktop protocols (VNC, RDP, SSH) to the web browser.
*   **Apache Guacamole Integration**: Directly utilizes `guacamole-common` libraries from Apache Guacamole, ensuring deep and compliant integration with the Guacamole ecosystem.
*   **Authentication and Security**:
    *   Integrates with `crczp-security-commons`, leveraging the platform's common security framework for authentication and authorization.
    *   Uses `Nimbus JOSE + JWT` for handling JSON Web Tokens, indicating robust token-based security for user sessions.
*   **Reactive and Traditional Web Support**: Includes `spring-boot-starter-web` and `spring-boot-starter-webflux`, suggesting it can handle both traditional blocking HTTP requests and more scalable reactive, non-blocking requests.
*   **API Documentation**: Uses `Springdoc OpenAPI UI` for generating interactive API documentation, detailing the endpoints and functionalities offered by this service.
*   **Data Persistence**: Uses `spring-boot-starter-jdbc` and has a runtime dependency on `PostgreSQL` for data storage, likely for session information or configuration.
*   **Network Optimization**: Dependency management for various `netty-*` components points to efficient, low-level network communication, essential for high-performance WebSocket handling.
*   **High Code Quality**: Adheres to the platform's rigorous code quality and security standards through integrated build tools like Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check.

## Role in CyberRangeCZ:

The `backend-guacamole` service is critical for user interaction with the sandbox environments:

*   **Secure Remote Access**: Provides a secure and authenticated channel for trainees to access their virtual machines directly through a web browser, eliminating the need for client-side VPNs or RDP/SSH clients.
*   **Simplified User Experience**: Offers a clientless solution that is accessible from anywhere with a web browser, enhancing the usability of the CyberRangeCZ platform.
*   **Centralized Control**: Allows the platform to manage and control access to sandbox resources, apply session policies, and monitor remote desktop activity.
*   **Scalability**: The use of WebSockets and potentially reactive programming enables the service to handle a large number of concurrent remote access sessions efficiently.

This service is a cornerstone of the user-facing interaction with the training environments, providing a flexible, secure, and integrated remote access solution.
