# ansible-role-interface

This repository contains an Ansible role for comprehensive network interface configuration on Debian-based systems. It allows for detailed and automated setup of network parameters, which is critical for establishing the desired network topology and connectivity within the CyberRangeCZ training environments.

## Key Features:

*   **Network Interface Configuration**: The role enables the configuration of various aspects of network interfaces, including:
    *   **MAC Address Identification**: Interfaces are identified by their MAC address, ensuring precise targeting.
    *   **IP Addressing**: While not explicitly shown in the `README.md` example, standard network interface configuration usually implies setting IP addresses (which would typically be handled within the `interface_interfaces` structure or a dependent task).
    *   **Default Gateway**: Configuration of a default IPv4 gateway for specific interfaces.
    *   **Static Routes**: Ability to define static routes with a gateway, network, and subnet mask.
    *   **MTU (Maximum Transmission Unit)**: Customizable MTU settings, defaulting to `1442`, which is often used in virtualized or overlay networks to prevent fragmentation issues.
*   **Configuration Cleaning**: An optional `interface_clean` parameter allows for clearing existing network interface configurations before applying new ones, ensuring a clean slate.
*   **Custom Configuration File**: The `interface_file_name` parameter provides flexibility to specify a custom file name for the interface configuration within `/etc/network/interfaces.d/`.
*   **Requires Root Access**: Network configuration changes require `become: yes` (root privileges) to be set.
*   **Requires Gathered Facts**: Relies on Ansible's gathered facts for dynamic configuration.

This role is fundamental for creating and managing the diverse and isolated network environments characteristic of a cyber range, ensuring that virtual machines are correctly networked and accessible for training scenarios.
