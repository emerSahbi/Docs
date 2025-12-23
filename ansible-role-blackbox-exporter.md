# ansible-role-blackbox-exporter

This repository contains an Ansible role that installs and configures the [Prometheus Blackbox Exporter](https://github.com/prometheus/blackbox_exporter) on a Kubernetes cluster. The Blackbox Exporter is used for black-box monitoring, allowing you to probe endpoints over protocols like HTTP, HTTPS, DNS, TCP, and ICMP to verify that they are working correctly.

This Ansible role automates the deployment of the Blackbox Exporter using a Helm chart from the `prometheus-community` repository.

## Key Features:

*   **Helm-based Deployment**: The role uses Helm to deploy the `prometheus-blackbox-exporter` chart, which simplifies the installation and configuration process.
*   **Kubernetes Integration**: It is designed to work with a Kubernetes cluster, specifically mentioning `k3s` clusters.
*   **Namespace Management**: It creates a `prometheus` namespace for the exporter if it doesn't already exist.
*   **Service Exposure**: It exposes the Blackbox Exporter using a `LoadBalancer` service, making it accessible for Prometheus to scrape.
*   **Default Probes**: It comes with pre-configured probing modules for common use cases, including:
    *   `http_2xx`: To check for successful HTTP responses.
    *   `tcp`: To check if a TCP port is open.
    *   `icmp`: To perform ping checks.

This role is a dependency for other monitoring-related components in the CyberRangeCZ platform, providing a standardized way to set up black-box monitoring.
