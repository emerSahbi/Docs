# ansible-role-windows-exporter

This repository contains an Ansible role dedicated to installing the [Prometheus Windows Exporter](https://github.com/prometheus-community/windows_exporter) on Windows target systems. The Windows Exporter is an agent that exposes a variety of hardware and operating system metrics from Windows machines, making them available for collection by a Prometheus server. This provides crucial visibility into the health and performance of Windows-based components within the CyberRangeCZ platform.

## Key Features:

*   **Windows Exporter Installation**: The role uses the `ansible.windows.win_package` module to download and install the official Windows Exporter `.msi` package from its GitHub releases.
*   **Default Listening Port**: During installation, it configures the Windows Exporter to listen on port `9100`, which is the conventional port for Prometheus exporters. This ensures compatibility with standard Prometheus scraping configurations.
*   **Simple and Direct**: The role focuses solely on the installation of the exporter with a few basic configurations, implying that further Prometheus-side configurations (like scrape jobs) would be handled by other roles (e.g., `ansible-role-prometheus`).
*   **Enables Windows Monitoring**: By deploying the Windows Exporter, this role enables the collection of essential Windows system metrics (e.g., CPU, memory, disk I/O, network, services status), which are vital for comprehensive monitoring in mixed-OS training environments.

## Importance in CyberRangeCZ:

This role is important for the CyberRangeCZ platform as it allows for:

*   **Unified Monitoring**: Extends the Prometheus-based monitoring infrastructure to include Windows operating systems, providing a consistent monitoring experience across the entire range of virtual machines.
*   **Support for Windows Scenarios**: Critical for training scenarios that involve Windows servers or workstations, allowing instructors and monitoring systems to track the state and behavior of these systems.
*   **Performance and Health Insights**: Provides valuable data for diagnosing issues, understanding resource utilization, and validating the impact of actions within Windows-based training exercises.

This role ensures that Windows systems are not a "black box" in the monitoring landscape of the CyberRangeCZ, providing essential observability.
