# ansible-role-sandbox-logging-bash

This repository contains an Ansible role specifically designed to implement local terminal command logging for Bash shells within the CyberRangeCZ sandbox environments. This role is a critical component for monitoring and auditing trainee activity, providing insights into the commands they execute during exercises.

## Key Features:

*   **Bash Command Logging**: Captures and logs commands executed in Bash shells, including commands run within nested shells.
*   **Operating System Support**: Tested and supported on various Linux distributions, including Ubuntu 20.04, Debian 10, Kali Linux 2019.4, and CentOS 8.
*   **Root Access Required**: Modifying shell configurations and logging mechanisms requires elevated privileges (`become: yes`).
*   **Script Execution Logging**: Logs the execution of shell scripts (e.g., `./myscript.sh`), but not the individual commands contained within the script itself.
*   **No Role Parameters**: The role is designed to be used without specific parameters, simplifying its application.
*   **Extensibility**: The `README.md` hints at potential future enhancements, such as logging terminal output (`stdout`/`stderr`) or process IDs for more granular activity tracking.

## Importance in CyberRangeCZ:

This role is indispensable for educational and assessment purposes within the CyberRangeCZ platform. By logging terminal commands, instructors can:

*   **Monitor Trainee Progress**: Understand how trainees are interacting with the environment and whether they are following intended procedures or exploring alternative solutions.
*   **Identify Learning Gaps**: Pinpoint areas where trainees might be struggling or making incorrect assumptions.
*   **Facilitate Post-Exercise Debriefing**: Review command histories to provide targeted feedback and evaluate performance against exercise objectives.
*   **Maintain Audit Trails**: Create a record of actions performed within the sandbox, which can be valuable for incident response training and forensic analysis.

This ensures a controlled and observable training environment where learning outcomes can be effectively measured and supported.
