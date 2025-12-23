# ansible-stage-one-testing-definition

This repository contains the testing definitions and playbooks for validating the `ansible-stage-one` provisioning process. It defines a complex virtual machine topology and executes a series of integration tests to ensure that the initial setup of the CyberRangeCZ sandbox environment, encompassing both Linux and Windows systems, is successful and functional.

## Key Components:

*   **`topology.yml`**: This file defines the intricate structure of the test environment. It specifies:
    *   A diverse set of **Linux hosts** (e.g., Kali, Debian, Ubuntu) and **Windows hosts** (e.g., Windows Server 2019, Windows 10, Windows 7) with their respective base images, management users, and compute flavors.
    *   Various **router images** (e.g., OPNsense, Debian-based routers).
    *   Multiple isolated **networks** with defined CIDR ranges.
    *   Detailed **network mappings** that connect hosts and routers to specific networks with static IP addresses, establishing the overall network architecture for testing.
    *   Placeholder groups for monitoring (`monitor-os`, `monitor-icmp`), indicating potential integration points for monitoring verification.
*   **`provisioning/playbook.yml`**: This Ansible playbook executes the actual tests against the environment defined by `topology.yml`. It performs a series of comprehensive checks:
    *   **Linux Connectivity Tests**: Verifies internet connectivity (ping `8.8.8.8`), DNS resolution (ping `seznam.cz`), and outbound HTTPS access (`curl https://www.powershellgallery.com`) for Linux SSH nodes. These tests are performed both before and after a system reboot to ensure persistence and stability.
    *   **Windows WinRM Connectivity Tests**: Confirms that Ansible can successfully connect and execute commands on Windows hosts using WinRM (Windows Remote Management) via `win_ping`. These tests are also performed post-reboot.
    *   **Windows SSH Connectivity Tests**: Uniquely, the playbook also includes tests to verify SSH access to Windows machines, suggesting the presence and configuration of an SSH server on these Windows VMs. Similar connectivity checks (ping, `Invoke-WebRequest`) are performed via SSH.

## Purpose and Importance:

The `ansible-stage-one-testing-definition` repository is vital for maintaining the quality and reliability of the CyberRangeCZ platform:

*   **Ensures Robust Initial Setup**: By thoroughly testing network connectivity, service availability, and system responsiveness across various operating systems, it verifies that the `ansible-stage-one` playbook correctly provisions the foundational environment.
*   **Validates Heterogeneous Environments**: Confirms that the platform can successfully deploy and manage both Linux and Windows virtual machines, which is essential for creating realistic and diverse cybersecurity training scenarios.
*   **Automated Quality Assurance**: Provides an automated mechanism to detect regressions or issues in the `ansible-stage-one` playbook, especially when changes are introduced to the underlying infrastructure or Ansible roles.

In essence, this repository acts as the quality gate for the initial setup phase, guaranteeing that the complex environments required for the cyber range are consistently and correctly deployed.
