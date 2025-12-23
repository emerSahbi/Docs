# backend-topology-definition

This repository contains `cyberrangecz-topology-definition`, a Python package (library) whose core purpose is to **define the data models and schema for CyberRange topologies**. In the context of the CyberRangeCZ platform, this library provides a standardized way to describe the structure and configuration of isolated training environments (sandboxes), including their virtual machines, networks, and interconnections.

## Key Features:

*   **Topology Data Models**: Provides Python classes and data structures that represent the various components of a CyberRange topology (e.g., hosts, routers, networks, network mappings, resource requirements).
*   **Schema for Sandbox Definitions**: Serves as the authoritative schema for how sandbox definitions are structured. This is crucial for ensuring consistency when different parts of the platform (like the `backend-sandbox-service` or frontend components) create, manage, or display sandbox layouts.
*   **Code Reusability**: By centralizing topology definitions, it prevents duplication and ensures that all components operate with a common understanding of what a "topology" entails.
*   **Language-Agnostic Representation (Implicit)**: While implemented in Python, the underlying concepts and potentially the serialization format (e.g., to YAML or JSON) would allow for platform-wide understanding of these topologies.
*   **Python Library**: Designed as an installable Python package, intended to be a dependency for other Python-based services that need to work with CyberRange topologies.

## Role in CyberRangeCZ:

The `backend-topology-definition` library is fundamental to the platform's ability to create, manage, and present complex training environments:

*   **Enables Structured Sandbox Creation**: Provides the framework for `backend-sandbox-service` to process and deploy sandbox definitions by giving a clear structure to these definitions.
*   **Consistency Across the Platform**: Ensures that the definition of a network, a host, or a connection is uniform across all services that interact with topology information.
*   **Foundation for IaC**: Directly supports the "Infrastructure as Code" approach by defining the logical structure of the infrastructure that will be provisioned by tools like Terraform/OpenTofu or OpenStack Heat (as driven by `backend-terraform-client` or `backend-openstack-lib`).
*   **Facilitates Visualization**: Frontend components that visualize network topologies would likely consume definitions adhering to this library's schema, ensuring accurate and consistent graphical representations.

This library acts as a crucial "contract" for the structure of cyber range environments, enabling systematic and automated management of training sandboxes.
