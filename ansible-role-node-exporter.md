# ansible-role-node-exporter

This repository contains an Ansible role for installing and configuring the [Prometheus Node Exporter](https://github.com/prometheus/node_exporter) on Linux systems, with specific tasks for Debian/RedHat and FreeBSD operating system families. The Node Exporter is a critical component for monitoring server-level metrics, exposing a wealth of information about the underlying operating system and hardware to a Prometheus server.

## Key Features:

*   **Multi-OS Support**: The role includes conditional logic to apply appropriate installation steps based on the operating system family (Debian/RedHat and FreeBSD).
*   **Automated Installation**:
    *   Downloads a specific version of the Node Exporter (e.g., `v1.3.1`) directly from the official GitHub releases.
    *   Extracts the executable and places it in `/usr/local/bin`.
*   **Systemd Service Management**:
    *   Creates a `systemd` service file for Node Exporter, ensuring it runs as a managed service.
    *   Allows for custom command-line arguments to be passed to the Node Exporter via the `service_parameters` variable.
*   **Service Control**: Includes handlers to gracefully restart the Node Exporter service when configuration changes are applied, ensuring the new settings take effect.
*   **Enables Monitoring**: By deploying the Node Exporter, this role enables the collection of essential system metrics (CPU usage, memory, disk I/O, network statistics, etc.), which are vital for monitoring the health and performance of the CyberRangeCZ platform's infrastructure.

This role ensures that all participating nodes in the CyberRangeCZ environment are properly instrumented for monitoring, providing the necessary data for performance analysis, troubleshooting, and maintaining overall system stability.
