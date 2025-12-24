# backend-security-commons

This repository provides a common security library for other backend microservices within the CyberRangeCZ platform. It is a Java-based Spring Boot project designed to be included as a Maven dependency in other services to provide a standardized approach to security and service registration.

## Key Functionality:

*   **Centralized Security Configuration**: This library centralizes security configurations, ensuring that all microservices adhere to the same security standards. It provides pre-configured settings for OAuth2 resource server, CORS, and CSRF protection.
*   **Microservice Auto-Registration**: It includes functionality for a microservice to automatically register itself with the central `user-and-group` service upon startup. This allows for dynamic discovery and management of microservices within the platform.
*   **Standardized Role Management**: The library enforces a consistent model for role management. Services that consume this library define their roles in a `roles.json` file, which is then used by the security commons to manage access control.
*   **OAuth2 Resource Server Integration**: By importing the `ResourceServerSecurityConfig`, a microservice is configured as an OAuth2 resource server, capable of validating access tokens from an identity provider.
*   **Simplified Integration**: Developers can easily integrate these security features into their microservices by adding the appropriate `@Import` annotations and configuring the necessary properties.

## Role in CyberRangeCZ:

The `backend-security-commons` library is a foundational component of the CyberRangeCZ backend architecture. It plays a crucial role in:

*   **Enhancing Security**: By providing a common security framework, it reduces the risk of security misconfigurations in individual microservices.
*   **Improving Developer Productivity**: It abstracts away the complexity of security implementation, allowing developers to focus on business logic.
*   **Ensuring Consistency**: It ensures that all backend services follow the same security and registration protocols, making the overall system more robust and maintainable.

In essence, this library acts as a security and integration backbone for the CyberRangeCZ platform, providing the necessary tools to build secure and interoperable microservices.
