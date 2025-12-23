# docker-dependencies-mirror

This repository plays a crucial role in the CyberRangeCZ platform's build and deployment ecosystem by providing **unmodified mirrors of essential upstream Docker images** hosted on the GitHub Container Registry (GHCR). The primary motivations for maintaining these mirrors are to enhance build reliability, ensure consistent access to dependencies, and mitigate potential issues arising from Docker Hub rate limiting or changes in upstream availability.

## Key Functionality:

*   **Reliable Dependency Source**: Acts as a trusted, internal source for critical third-party Docker images. By mirroring these images, the CyberRangeCZ platform reduces its dependency on external registries and enhances the predictability of its build processes.
*   **Mitigation of Docker Hub Rate Limiting**: Docker Hub's rate limits can sometimes impede CI/CD pipelines. By serving mirrored images from GHCR, this repository helps circumvent these limitations, ensuring faster and more consistent builds.
*   **Unmodified Mirrors**: The `README.md` explicitly states that these are "unmodified mirrors" of the official upstream releases, meaning the integrity and functionality of the original images are preserved.
*   **Centralized Mirroring**: Centralizes the process of maintaining these mirrored images, making it easier to manage and update them as new upstream versions become available.

## Mirrored Services:

The repository currently mirrors Docker images for the following services, which are widely used components within the CyberRangeCZ platform:

*   **Redis**: An in-memory data structure store, used as a database, cache, and message broker by various backend services.
*   **Syslog-ng**: A powerful and flexible log management solution, likely used in conjunction with the platform's logging forwarding roles (e.g., `ansible-role-man-logging-forward`).
*   **Guacamole (`guacd`)**: The backend daemon for Apache Guacamole, responsible for handling remote desktop protocols, crucial for browser-based access to sandboxes.

## Role in CyberRangeCZ:

This repository is fundamental to the operational robustness of the CyberRangeCZ platform:

*   **Ensures Build Stability**: Guarantees that the platform's microservices and other containerized components can be built consistently, even if external image sources experience issues.
*   **Optimizes CI/CD Performance**: By providing local or faster-access mirrors, it can significantly reduce image pull times during CI/CD pipelines, accelerating development and deployment cycles.
*   **Supply Chain Security**: Offers greater control over the Docker images consumed by the platform, potentially allowing for internal scanning or verification processes before usage.

By centralizing and mirroring key Docker dependencies, this repository contributes to a more resilient, efficient, and secure software supply chain for the entire CyberRangeCZ ecosystem.
