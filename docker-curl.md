# docker-curl

This repository defines a Docker image that extends a base `rancher/curl` image by adding the `jq` command-line JSON processor. The resulting image provides a convenient and powerful toolset for interacting with RESTful APIs and processing JSON data in containerized environments.

## Key Features:

*   **`curl` Utility**: Inherits the `curl` command-line tool from its base image (`rancher/curl:latest`), enabling making HTTP requests, transferring data with various protocols, and debugging network issues.
*   **`jq` for JSON Processing**: Adds `jq`, a lightweight and flexible command-line JSON processor. This allows for parsing, filtering, mapping, and transforming JSON data returned by APIs directly within the shell.
*   **Containerized Environment**: Provides a consistent and isolated environment for executing `curl` and `jq` commands, making it ideal for:
    *   **CI/CD Pipelines**: Performing API tests, fetching configuration from services, or triggering webhooks.
    *   **Scripting and Automation**: Automating tasks that involve API interactions in shell scripts.
    *   **Debugging**: Quickly inspecting API responses and extracting relevant information.

## Role in CyberRangeCZ:

Within the CyberRangeCZ platform, this `docker-curl` image is likely used in various automation and scripting contexts:

*   **API Interaction**: Used by DevOps scripts, CI/CD pipelines, or other automation components to interact with the platform's microservices APIs (e.g., triggering sandbox creation, querying service status, fetching data from backend services).
*   **Testing**: Essential for writing automated tests that validate the functionality of RESTful APIs by sending requests and asserting on the JSON responses.
*   **Debugging and Troubleshooting**: Provides a handy tool for developers and administrators to quickly diagnose issues and inspect data flows in a containerized environment.

This simple yet effective utility image streamlines operations and development workflows by providing readily available tools for API-centric tasks.
