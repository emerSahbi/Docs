# ansible-role-common

This repository contains a special kind of Ansible role that is not meant to be executed directly. Instead, it serves as a library of reusable Jinja2 macros that can be imported and used by other Ansible roles.

The primary purpose of this role is to provide a set of helper functions for common network-related tasks, making it easier to work with network interface information gathered from Ansible facts.

## Key Features:

*   **Jinja2 Macros**: The core of this role is the `templates/network.j2` file, which contains several macros for network interface manipulation, including:
    *   `mac_to_interface(mac)`: Finds the name of a network interface (e.g., `eth0`) based on its MAC address.
    *   `ip_to_interface(ip)`: Finds the name of a network interface based on its IP address.
    *   `get_inactive_interfaces()`: Returns a list of all network interfaces that are currently inactive.
*   **Dependency on Ansible Facts**: The macros in this role rely on the network information gathered by Ansible's fact-gathering mechanism. Therefore, it is important to have `gather_facts: yes` enabled when using these macros.

By providing these reusable macros, the `ansible-role-common` repository helps to avoid code duplication and simplifies network-related automation tasks in other Ansible roles within the CyberRangeCZ project.
