# backend-openstack-lib

This repository contains `cyberrangecz-openstack-lib`, a Python library specifically developed to serve as an **OpenStack cloud driver** for the CyberRangeCZ platform. It provides the necessary tools and abstractions to interact with OpenStack APIs, enabling the platform to provision, manage, and orchestrate sandbox environments within an OpenStack cloud infrastructure. This library is the OpenStack counterpart to `backend-aws-lib`, providing multi-cloud deployment capabilities to the platform.

## Key Features:

*   **OpenStack Cloud Driver**: Offers a specialized driver for OpenStack, allowing other services (such as the `sandbox-service`) to programmatically manage OpenStack resources.
*   **Heat Stack Manipulation**: The core functionality revolves around the `ostack_client` module, which provides functions for manipulating OpenStack Heat stacks. Heat is OpenStack's orchestration service, enabling the deployment of entire application topologies (like a sandbox environment) from a single template (Infrastructure as Code). This implies the library is used to launch and manage complex virtual infrastructures.
*   **Utility Functions**: Includes a `utils` module for common helper functions and an `exceptions` module for custom error handling.
*   **Sandbox Definitions**: The presence of `sandbox.yaml` and `small-sandbox.yaml` files within the repository suggests that these are example Heat templates or similar definitions that this library would process to deploy specific sandbox configurations.
*   **Installable Component**: Designed as an installable Python package, intended to be consumed by other applications within the CyberRangeCZ ecosystem.

## Role in CyberRangeCZ:

The `backend-openstack-lib` is a critical component for the CyberRangeCZ platform's multi-cloud strategy and its ability to deliver flexible training environments:

*   **Enables OpenStack Backend**: Allows the platform to utilize OpenStack as a cloud provider for deploying and hosting cybersecurity training sandboxes, offering an alternative to AWS.
*   **Infrastructure as Code Orchestration**: Provides the means to deploy complex virtual environments (sandboxes) using OpenStack Heat templates, ensuring consistency, repeatability, and automation.
*   **Abstraction Layer**: Abstracts the complexities of direct OpenStack API calls, simplifying the development of cloud-agnostic sandbox management logic.
*   **Resource Management**: Facilitates the automated creation, modification, and deletion of OpenStack resources such as virtual machines, networks, routers, and security groups.

By offering a robust and integrated OpenStack driver, this library significantly contributes to the flexibility, scalability, and cost-effectiveness of the CyberRangeCZ platform by supporting a major open-source cloud infrastructure.
