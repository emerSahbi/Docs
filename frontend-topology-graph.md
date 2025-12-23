# frontend-topology-graph

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"Topology Graph Component"**, an Angular library specifically designed to **visualize network graph topologies using D3.js** within the CyberRangeCZ platform. Its primary goal was to provide a dynamic and interactive graphical representation of sandbox environments, making it easier for users (both trainees and instructors) to understand the complex network layouts, virtual machines, and connections.

## Historical Functionality:

*   **Interactive Network Visualization**: Renders network topologies as interactive graphs, allowing users to explore the connections between various virtual machines and network segments.
*   **D3.js Powered**: Leverages the powerful D3.js library for creating sophisticated and data-driven graphical visualizations. (Likely used in conjunction with `frontend-d3-service`).
*   **Dynamic Data Fetching**: Fetches topology data from the `backend-sandbox-service`, ensuring that the visualization reflects the current state of the sandbox.
*   **Polling for Updates**: Supports a configurable polling period to automatically update the graph, reflecting real-time changes in the sandbox topology.
*   **Guacamole Integration**: Includes configuration for Guacamole services (URL, username, password), indicating that the visualization could potentially provide direct links or context for remote access to VMs within the graph.
*   **Customizable Assets**: Allows for custom icons and assets to represent different network elements, enhancing the clarity and branding of the visualization.
*   **Error and Loading States**: Provides services to display loading indicators and error messages, improving the user experience during data fetching.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **D3.js**: A JavaScript library for producing dynamic, interactive data visualizations.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, this topology graph component was critical for enhancing the user's understanding and interaction with the complex training environments:

*   **Improved Situational Awareness**: Provided a clear visual overview of the sandbox network, which is essential for trainees to understand the attack surface or for instructors to monitor the environment.
*   **Facilitated Training**: Helped trainees navigate and understand the network structure during exercises, especially in scenarios involving multiple interconnected VMs.
*   **Simplified Troubleshooting**: Allowed administrators to quickly visualize and diagnose network configurations and connectivity issues.

Its integration into the `frontend-platform` monorepo signifies a consolidation of frontend development efforts, centralizing various visualization components into a single, cohesive codebase for improved maintenance and a more integrated user experience.
