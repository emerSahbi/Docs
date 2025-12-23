# ansible-role-sandbox-logging

This repository contains a master Ansible role designed to manage the logging configuration for hosts within the CyberRangeCZ sandbox environments. It acts as an orchestrator, integrating and facilitating the use of several specialized sub-roles to capture, process, and forward various types of logs. This comprehensive logging setup is essential for monitoring activities, assessing trainee performance, and conducting forensic analysis during cyber training exercises.

## Key Features:

*   **Master Role for Logging**: This role serves as a central point for configuring host-level logging across the sandbox.
*   **Integration with Sub-roles**: It leverages and manages the following dedicated logging sub-roles:
    *   [`ansible-role-sandbox-logging-bash`](https://github.com/cyberrangecz/ansible-role-sandbox-logging-bash.git): Configures logging for terminal commands executed via Bash/ZSH, capturing user activity.
    *   [`ansible-role-sandbox-logging-msf`](https://github.com/cyberrangecz/ansible-role-sandbox-logging-msf.git): Sets up logging for Metasploit commands, crucial for tracking offensive security tool usage.
    *   [`ansible-role-sandbox-logging-forward`](https://github.com/cyberrangecz/ansible-role-sandbox-logging-forward.git): Manages the forwarding of local logs from the sandbox host to a specified remote log collection host (e.g., a SIEM or central logging server).
*   **Environment-Aware Configuration**: Automatically detects and adjusts configurations based on whether the sandbox is running in a local or cloud environment. It sets the `slf_local_env` parameter for the `sandbox-logging-forward` sub-role accordingly.
*   **Requires Root Access & Fact Gathering**: The role requires elevated privileges (`become: yes`) to modify system-level logging configurations and relies on Ansible's gathered facts for proper operation.
*   **Parameter Overrides**: While the master role itself has no direct parameters, it allows overriding parameters defined within its sub-roles, offering flexibility for specific logging needs.

## Usage & Importance:

This role is critical for the CyberRangeCZ platform because it ensures that all significant actions and events within the training sandboxes are captured. This includes user commands, security tool usage, and system-level events. By forwarding these logs to a central location, trainers can gain deep insights into trainee behavior, identify learning gaps, and review actions taken during exercises. It also supports post-exercise analysis and validation. The role also highlights the importance of time synchronization, recommending the use of the `ansible-role-chrony` for accurate log timestamps.
