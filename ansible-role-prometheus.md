# ansible-role-prometheus

This repository contains a comprehensive Ansible role for deploying and configuring Prometheus, the open-source monitoring and alerting toolkit, within the CyberRangeCZ platform. This role goes beyond a basic installation, setting up a robust monitoring solution that dynamically discovers targets and integrates with other monitoring components.

## Key Features:

*   **Helm-based Deployment**: Deploys the `kube-prometheus-stack` Helm chart (specifically Prometheus, with Alertmanager and Grafana disabled by default) to a `k3s` Kubernetes cluster. This leverages Helm for simplified and repeatable deployments.
*   **Dynamic Scrape Target Discovery**:
    *   **Node Exporter Integration**: Automatically identifies and configures scrape targets for `node-exporter` instances across the inventory, allowing Prometheus to collect system-level metrics (CPU, memory, disk, network).
    *   **Blackbox Monitoring (ICMP & TCP)**: Sets up `blackbox-exporter` jobs for ICMP (ping) and TCP port monitoring. This is crucial for checking the availability and reachability of services from an external perspective. It relies on the `ansible-role-blackbox-exporter` for the `prometheus-blackbox-exporter` service.
*   **Customizable Scrape Configurations**: Allows for injecting custom scrape configurations and relabeling rules through variables (`custom_os_metric_relabel_configs`, `custom_os_relabel_configs`, `customScrapeConfigs`), providing flexibility for specific monitoring needs.
*   **Service Exposure**: Configures the Prometheus service within Kubernetes as a `LoadBalancer`, making the Prometheus UI accessible.
*   **Kubernetes Integration**: Designed to operate within a Kubernetes environment, specifically utilizing `k3s` cluster kubeconfig for deployments.

This role is a central piece of the CyberRangeCZ monitoring strategy, enabling the collection, storage, and querying of metrics from various components of the training environment, thereby facilitating performance analysis, health checks, and proactive issue detection.
