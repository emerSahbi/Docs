# ansible-stage-one

This repository contains a foundational Ansible playbook (`playbook.yml` within the `provisioning` directory) that represents the **initial provisioning and configuration stage** for virtual machines within the CyberRangeCZ sandbox environment. It is a comprehensive orchestration that sets up core infrastructure components, network connectivity, user access, and monitoring across a heterogeneous mix of Linux and Windows operating systems.

This "stage one" ensures that all virtual machines are in a ready state for subsequent, more specialized training scenarios or service deployments.

## Key Functionalities and Integrated Roles:

The `playbook.yml` orchestrates numerous tasks and integrates several dedicated Ansible roles (many of which have been documented previously) to achieve its goals:

1.  **Connectivity and Basic System Checks**:
    *   Verifies SSH connectivity to various node types (`management`, `routers`, `ssh_nodes`).
    *   Performs basic system checks, including attempting to extract DNS server information from `systemd-resolved`.

2.  **Network Configuration**:
    *   **Interface Configuration**: Utilizes the [`ansible-role-interface`](document/ansible-role-interface.md) to configure network interfaces on `management` and `routers` nodes, including MAC address mapping, default gateways, static routes, and MTU settings. It dynamically discovers and configures interfaces.
    *   **IP Forwarding**: Sets the `net.ipv4.ip_forward` sysctl parameter on routers to enable IP forwarding.
    *   **Netplan Configuration (Ubuntu/Debian)**: For specific Linux `ssh_nodes`, it generates and applies Netplan configurations for network setup, including DHCP and route metrics.

3.  **Essential Services Deployment on Management Node (`man`)**:
    *   Installs `chrony` and `guacd` (Guacamole Daemon) using `apt`.
    *   Configures `guacd` to listen on all interfaces (`0.0.0.0`) and restarts its service.
    *   **NAT Configuration**: Implements Network Address Translation (NAT) on the `man` node using the [`ansible-role-iptables`](document/ansible-role-iptables.md) role, masquerading outgoing traffic.
    *   **Logging Forwarding**: Configures log forwarding to a central "head" node using the [`ansible-role-man-logging-forward`](document/ansible-role-man-logging-forward.md) role.
    *   **Network Segmentation/Isolation**: Applies `iptables` DROP rules on the `man` node to restrict traffic from private IP ranges, enhancing network security and isolation for training environments.

4.  **User Access Management**:
    *   **Linux User Access**: Uses the [`ansible-role-user-access`](document/ansible-role-user-access.md) role to:
        *   Provision a `user` account on `man` and `uan` (User Accessible Nodes) with restricted SSH access.
        *   Provision `user` and `management` accounts on the `proxy-jump` host, also with restricted SSH.
        *   Provision a `user` account with a password and `sudo` privileges on `user_accessible_nodes`.
    *   **Windows User Access**: Utilizes the [`ansible-role-user-access-windows`](document/ansible-role-user-access-windows.md) role to:
        *   Provision a `user` account with a password and administrator privileges on `user_accessible_nodes` (Windows).
        *   Configures SSH access to Windows VMs by ensuring `.ssh` directories and authorized keys are present for the Ansible user.

5.  **Hostname and System Configuration Cleanup**:
    *   Removes stack name prefixes from hostnames and `/etc/hosts` files on both Linux and Windows nodes, making them cleaner and more consistent.
    *   Adjusts `cloud-init` configuration on Linux to prevent it from overwriting `/etc/hosts` changes.

6.  **Docker Environment Preparation**:
    *   Targets `docker_hosts`.
    *   Provisions a `crczp-user` with restricted SSH using [`ansible-role-user-access`](document/ansible-role-user-access.md).
    *   Installs `gnupg-agent` and `docker-compose` using the [`ansible-role-docker-compose`](document/ansible-role-docker-compose.md) role.
    *   Adds the Ansible user to the `docker` group.
    *   Copies Docker container definitions and builds them using `community.docker.docker_compose_v2`.

7.  **Monitoring Stack Deployment**:
    *   Deploys Prometheus using the [`ansible-role-prometheus`](document/ansible-role-prometheus.md) and Blackbox Exporter using the [`ansible-role-blackbox-exporter`](document/ansible-role-blackbox-exporter.md) on the `man` node.
    *   Deploys Node Exporter using the [`ansible-role-node-exporter`](document/ansible-role-node-exporter.md) on Linux hosts, conditionally targeting specific monitoring groups or all Linux hosts.
    *   Deploys Windows Exporter using the [`ansible-role-windows-exporter`](document/ansible-role-windows-exporter.md) on Windows hosts, similarly targeting specific monitoring groups or all Windows hosts.

## Overall Purpose:

`ansible-stage-one` is a crucial initial setup phase that transforms raw virtual machines into a functional, interconnected, and monitored environment ready for complex cybersecurity training scenarios. It automates a significant amount of the infrastructure setup, ensuring consistency and reducing manual effort for deploying the CyberRangeCZ platform.
