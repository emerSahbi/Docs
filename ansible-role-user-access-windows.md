# ansible-role-user-access-windows

This repository contains an Ansible role specifically designed for managing user access on Windows-based systems within the CyberRangeCZ sandbox environments. It serves as the Windows counterpart to the `ansible-role-user-access` role, providing similar functionalities tailored for the Windows operating system.

## Key Features:

*   **User Account Provisioning**: Creates or manages a user account on the Windows target machine.
*   **SSH Key Management**: Although primarily for Windows, the role *mentions* setting a user's public SSH key as an authorized key. This implies that target Windows machines might have an SSH server (like OpenSSH for Windows) installed, allowing for secure, key-based authentication.
*   **Password Configuration**: Optionally sets a password for the provisioned user account (`user_access_password`).
*   **Administrator Privileges**: Can grant administrator rights to the user account (`user_access_admin: True`), which is essential for trainees requiring elevated permissions for certain exercises.
*   **RDP Access Control**: Configures Remote Desktop Protocol (RDP) access for the target system (`user_access_rdp: True`), enabling graphical remote access for trainees.
*   **Customizable Username**: The default username is `user-access`, but it can be changed via the `user_access_username` parameter.
*   **Requires Administrator Access**: Actions involving user management and system configuration on Windows require elevated privileges.

## Importance in CyberRangeCZ:

This role is crucial for integrating Windows virtual machines into the CyberRangeCZ training platform:

*   **Diverse Environment Support**: Ensures consistent user access management across both Linux and Windows operating systems within the training range.
*   **Automated Windows User Setup**: Streamlines the process of provisioning users on Windows targets, which can often be more complex than on Linux.
*   **Enabling Windows-Specific Exercises**: Facilitates training scenarios that specifically require interaction with Windows environments, such as Active Directory exploitation, malware analysis on Windows, or forensic investigations.
*   **Secure Remote Access**: Provides secure RDP and potentially SSH access for trainees to Windows machines.

By automating Windows user access, this role ensures that a wide array of realistic cybersecurity scenarios involving different operating systems can be effectively set up and managed.
