# ansible-role-user-access

This repository contains an Ansible role specifically designed for managing user access within the CyberRangeCZ sandbox environments. Its primary function is to secure and streamline how users, typically trainees, gain access to the virtual machines or systems provisioned for their exercises.

## Key Features:

*   **SSH Key Management**: The role facilitates secure access by setting a user's public SSH key as an authorized key. This allows users to connect to the target machines via SSH without requiring a password, enhancing security and convenience. The public key path can be configured via `user_access_ssh_public_key`.
*   **Optional Password Setting**: While SSH keys are preferred for security, the role provides an optional parameter (`user_access_password`) to set a password for the target user, which might be useful for certain scenarios or legacy systems.
*   **Customizable Username**: The default username is `user-access`, but it can be overridden using the `user_access_username` parameter.
*   **SSH Key Options**: Advanced SSH access controls can be applied through the `user_access_ssh_public_key_options` parameter, allowing for fine-grained permissions (e.g., restricting commands, forcing pseudo-terminals).
*   **Requires Root Access**: Managing user accounts and SSH configurations requires elevated privileges, so the role must be executed with `become: yes`.

## Importance in CyberRangeCZ:

This role is fundamental for the operation of the CyberRangeCZ platform because it:

*   **Enables Secure Access**: Provides a secure and auditable method for trainees to access their assigned sandbox resources.
*   **Automates User Provisioning**: Simplifies the process of setting up new user accounts and access credentials across potentially many virtual machines.
*   **Standardizes Access Control**: Ensures consistent application of access policies across different training environments.
*   **Supports Other Logging Roles**: As noted in `ansible-role-sandbox-logging-msf`, ensuring users are known to the system by this role is a prerequisite for comprehensive logging of their activities.

By effectively managing user access, this role contributes to both the security and usability of the CyberRangeCZ training infrastructure.
