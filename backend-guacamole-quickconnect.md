# backend-guacamole-quickconnect

**Note: This repository has been archived, and its ongoing development and functionality are now maintained within the `backend-guacamole` repository.**

This repository previously contained a modified version of the `guacamole-auth-quickconnect` extension for Apache Guacamole. Its purpose was to enhance the user experience by providing a simplified "quick connect" bar directly on the Guacamole Client's home page.

## Historical Functionality:

*   **Quick Connection Bar**: Enabled users to directly input a server URI (e.g., `rdp://hostname` or `ssh://username@hostname`) on the Guacamole interface to establish an immediate remote desktop connection.
*   **Guacd Proxy Parameters**: A key modification from the original Apache extension was the added ability to specify `guacd-hostname` and `guacd-port` as proxy parameters. This allowed the quick connect feature to work seamlessly with `guacd` instances that might be running on different hosts or ports, which is common in complex, containerized, or distributed environments like CyberRangeCZ sandboxes.
*   **JAR-based Deployment**: The extension was built as a `.jar` file and was intended to be mounted directly into the Guacamole Docker container, extending its capabilities.

## Role in CyberRangeCZ (Historical Context):

Historically, this extension would have contributed to the usability of the CyberRangeCZ platform by:

*   **Streamlining Access**: Providing a rapid way for trainees or administrators to connect to sandbox machines without pre-configuring each connection.
*   **Flexibility**: Allowing dynamic connections to various resources, potentially useful for exploratory tasks or ad-hoc access during training.

However, its archiving signifies that its features have either been integrated into the main `backend-guacamole` service or superseded by other architectural approaches within the platform.
