# frontend-sandbox-agenda

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"CyberRangeCZ Platform Sandbox Agenda"**, an Angular-based frontend library providing components and services for **managing the lifecycle and scheduling of sandbox environments**. It served as the primary user interface developed to interact with the `backend-sandbox-service`, offering administrators and instructors the tools to oversee and control the provisioning and utilization of training sandboxes.

## Historical Functionality:

*   **Comprehensive Sandbox Management**: Provided UI components and services for:
    *   Defining and managing various **sandbox definitions** (blueprints for environments).
    *   Creating and overseeing **sandbox pools** (collections of ready-to-use sandboxes).
    *   Controlling individual **sandbox instances** (starting, stopping, resetting, deleting).
    *   Managing **sandbox allocation** and tracking different **allocation stages**.
*   **Smart-Dumb Architecture**: Followed a software design pattern separating presentational (dumb) components from logical (smart) components, promoting reusability and testability.
*   **Core UI Features**: Included default routing, error handling, notification services, and navigation, ensuring a complete and user-friendly management experience.
*   **Extensibility**: Designed to be highly customizable, allowing developers to override default services for custom behavior, error handling, and notification display.
*   **Integration with Backend**: Developed as the frontend for `backend-sandbox-service`. Its demo application required several other backend services to be running, including `backend-training`, `backend-adaptive-training`, `backend-user-and-group`, and `backend-mitre-technique-service`.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, this `frontend-sandbox-agenda` component was crucial for the operational management of the CyberRangeCZ platform. It provided:

*   **Centralized Control Interface**: A graphical interface for administrators and instructors to effectively manage the complex dynamics of sandbox provisioning and allocation.
*   **Streamlined Workflow**: Simplified the process of setting up and monitoring training environments, reducing manual effort.
*   **Visibility**: Offered insights into the status of sandbox resources, enabling efficient resource utilization and troubleshooting.

Its integration into the `frontend-platform` monorepo signifies a consolidation of frontend development efforts, centralizing various user management and scheduling components into a single, cohesive codebase for improved maintenance and user experience.
