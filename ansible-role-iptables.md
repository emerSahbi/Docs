# ansible-role-iptables

This repository contains an Ansible role for configuring and persistently saving `iptables` firewall rules on Linux systems. `iptables` is a critical component for managing network packet filtering and NAT (Network Address Translation) on Linux, providing robust control over network traffic entering, leaving, and passing through a system.

## Key Features:

*   **Firewall Rule Configuration**: The role allows for the definition and application of `iptables` rules across different tables (e.g., `filter`, `nat`, `mangle`, `raw`) and chains (e.g., `INPUT`, `OUTPUT`, `FORWARD`, `PREROUTING`, `POSTROUTING`).
*   **Persistence**: It ensures that the configured `iptables` rules are saved and reloaded automatically upon system reboot, maintaining the desired firewall state.
*   **Requires Root Access**: Modifying firewall rules requires elevated privileges, so the role must be executed with `become: yes`.
*   **Flexible Rule Definition**: The role accepts an optional `iptables_rules` parameter, which is a list of dictionaries. Each dictionary corresponds to an `iptables` module call in Ansible, allowing for highly flexible and detailed firewall configurations.

Within the CyberRangeCZ platform, this role is essential for:

*   **Network Segmentation**: Isolating different virtual machines or networks for specific training scenarios.
*   **Traffic Control**: Allowing or denying specific types of network traffic to simulate real-world network conditions.
*   **NAT Configuration**: Setting up NAT rules for internet access or internal network routing within the training environments.

This role provides the necessary infrastructure for implementing granular network security policies within the cyber range.
