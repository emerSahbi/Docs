# ansible-role-hosts-aliases

This repository contains an Ansible role responsible for managing and populating the `/etc/hosts` file on Linux-based target systems. The `/etc/hosts` file provides a simple, local mechanism for mapping hostnames to IP addresses, which can be crucial for network communication and service discovery in isolated or complex network environments like a cybersecurity training range.

## Key Features:

*   **Host Entry Management**: The role adds specified hostname-to-IP address mappings to the `/etc/hosts` file.
*   **Linux System Support**: It is designed to operate on Linux-based operating systems.
*   **Root Access Required**: Modifying the `/etc/hosts` file requires elevated privileges, so the role must be executed with `become: yes`.
*   **Configurable Host Mappings**: It takes a mandatory parameter, `hosts_aliases_nodes_ip`, which is a dictionary where keys are hostnames and values are their corresponding IP addresses. This allows for dynamic and flexible management of host entries.

Within the CyberRangeCZ platform, this role is likely used to ensure that various virtual machines and services can correctly resolve each other's hostnames without relying solely on a DNS server, especially in scenarios where DNS might be configured differently or when specific, controlled network environments are required for training.
