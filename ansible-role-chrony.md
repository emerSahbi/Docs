# ansible-role-chrony

This repository contains an Ansible role for setting up and configuring the `chrony` service on Debian-based Linux systems. `chrony` is a modern implementation of the Network Time Protocol (NTP) used to keep the system clock synchronized with a time server.

Proper time synchronization is critical in distributed systems like CyberRangeCZ for accurate logging, event correlation, and authentication.

## Key Features:

*   **Chrony Installation**: The role installs the `chrony` package.
*   **Timezone Configuration**: It sets the system's timezone. The default is `Etc/UTC`, but it can be customized (e.g., to `Europe/Prague`).
*   **NTP Server Configuration**: It configures `chrony` to synchronize with a specified NTP server or pool. The default is `1.debian.pool.ntp.org`.
*   **Service Management**: The role ensures that the `chrony` service is started and enabled to run on boot.

This role helps ensure that all servers and nodes within the CyberRangeCZ environment have consistent and accurate time, which is a fundamental requirement for a stable and reliable platform.
