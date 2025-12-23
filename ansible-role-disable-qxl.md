# ansible-role-disable-qxl

This repository contains a simple Ansible role designed to disable the `qxl` kernel module on a target machine and then restart it. This role is tested on Debian-like operating systems.

The `qxl` driver is a paravirtualized graphics driver for the QEMU virtual machine monitor. In some virtualized environments, especially in cloud platforms like OpenStack, disabling the QXL driver can be necessary to:

*   Improve graphical performance.
*   Resolve compatibility issues with remote desktop clients.
*   Ensure stability of the virtual machine.

## Key Features:

*   **Disables QXL Module**: The role blacklists the `qxl` kernel module to prevent it from loading on boot.
*   **Restarts the Machine**: After blacklisting the module, the role restarts the machine to ensure that the change takes effect.
*   **Requires Root Access**: This role needs to be run with root privileges to modify kernel module blacklists and restart the machine.

This role is a utility that is likely used during the provisioning of virtual machines in the CyberRangeCZ environment to ensure they are configured correctly for the specific virtualization platform being used.
