# ansible-role-man-logging-forward

This repository contains an Ansible role that configures a device to act as an intermediary logging forwarder. Its primary function is to listen for incoming syslog messages from other devices (specifically those configured with `sandbox-logging-forward`) and then forward these collected logs to a designated central log host, often referred to as the "head" node.

This role is a key component of the logging infrastructure in the CyberRangeCZ platform, facilitating centralized log collection and analysis, which is essential for monitoring activities and performing forensic analysis in cybersecurity training scenarios.

## Key Features:

*   **Syslog Listener**: Configures the target device to listen for syslog messages from specified sources.
*   **Log Forwarding**: Forwards the received logs to a central log host using TCP, adhering to the `RFC5424` syslog protocol standard.
*   **Requires Root Access**: Modifying system logging configurations requires elevated privileges, so the role must be executed with `become: yes`.
*   **Configurable Destination**: A mandatory parameter, `kmlf_destination`, specifies the resolvable hostname or IP address of the central log host.
*   **Flexible Source and Destination Parameters**:
    *   **Source Configuration**: Optional parameters (`kmlf_source_ip`, `kmlf_source_port`, `kmlf_source_protocol`, `kmlf_source_max_connections`) allow for detailed control over how the device listens for incoming logs.
    *   **Destination Configuration**: Optional parameters (`kmlf_destination_port`, `kmlf_destination_protocol`) allow customization of how logs are forwarded to the central host.

By enabling the systematic collection and forwarding of logs, this role plays a vital part in providing visibility into the actions and events occurring within the CyberRangeCZ training environments, aiding in both real-time monitoring and post-event analysis.
