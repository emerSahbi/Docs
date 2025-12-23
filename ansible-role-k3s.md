# ansible-role-k3s

This repository contains an Ansible role for the automated installation and configuration of `k3s`, a lightweight and certified Kubernetes distribution. This role is fundamental for establishing the Kubernetes cluster infrastructure that underpins many services within the CyberRangeCZ platform.

Beyond just `k3s`, the role also ensures the presence of essential tools for Kubernetes management and automation.

## Key Features:

*   **k3s Installation**: Installs a specified version of `k3s` using its official installation script (`get.k3s.io`), providing a quick and efficient way to deploy a Kubernetes cluster.
*   **Idempotency**: The role checks for existing `k3s` installations and skips the installation process if `k3s` is already present, ensuring that repeated executions do not cause unintended reconfigurations.
*   **Helm Installation**: Deploys `helm`, the package manager for Kubernetes, which is crucial for deploying and managing applications (like Prometheus Blackbox Exporter or Guacamole) on the cluster using Helm charts.
*   **Python3-yaml Installation**: Installs the `python3-yaml` package, which is often a dependency for various Kubernetes-related command-line tools and automation scripts, enabling programmatic interaction with YAML configuration files.
*   **Debian-based System Support**: Designed for Linux distributions that use `apt` for package management, such as Debian and Ubuntu.
*   **Configurable k3s Version**: Allows specifying the desired `k3s_version` (e.g., `v1.31.4+k3s1`), providing flexibility to use different Kubernetes versions.

This role is a foundational component for the CyberRangeCZ platform, enabling the rapid provisioning of Kubernetes environments required for microservices deployment, sandbox orchestration, and other containerized applications.
