# ansible-role-docker-compose

This repository contains an Ansible role for installing Docker Compose as a plugin for the Docker Engine on Debian-based systems. Docker Compose is a tool used for defining and running multi-container Docker applications. It allows users to define their application's services, networks, and volumes in a `docker-compose.yml` file, and then manage the entire application stack with single commands.

## Key Features:

*   **Docker Compose Plugin Installation**: The role installs the `docker-compose-plugin` package using the `apt` package manager. This integrates Docker Compose directly into the Docker CLI as a subcommand (e.g., `docker compose up`).
*   **Requires Root Access**: As with most system-level installations, this role requires root privileges to execute successfully.

This role provides a simple and efficient way to ensure that Docker Compose is available on target machines, which is essential for deploying and managing multi-container applications within the CyberRangeCZ platform.
