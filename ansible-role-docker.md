# ansible-role-docker

This repository contains an Ansible role for installing and configuring Docker on Debian-based systems.

While the role is simple, it performs a few important tasks to ensure that Docker is set up correctly for the CyberRangeCZ environment.

## Key Features:

*   **Docker Installation**: The role installs the `docker.io` package using the `apt` package manager, which provides the Docker engine.
*   **MTU Configuration**: It configures the Docker daemon by creating a `/etc/docker/daemon.json` file and setting the Maximum Transmission Unit (MTU) to `1442`. This is a common practice to prevent network-related issues that can occur in environments with network overlays, tunnels, or certain firewall configurations.
*   **Directory Creation**: It ensures that the `/etc/docker` directory exists before attempting to create the configuration file.

This role provides a standardized way to install Docker with a specific network configuration, which is likely important for the networking setup of the CyberRangeCZ platform.
