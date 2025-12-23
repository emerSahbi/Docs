# backend-sandbox-service

This repository contains the `sandbox-service` backend microservice, which is the **core orchestration component for managing the entire lifecycle of cybersecurity training sandboxes** within the CyberRangeCZ platform. It provides a comprehensive set of REST APIs that allow for the programmatic definition, creation, management, and deletion of isolated training environments, integrating seamlessly with underlying cloud providers and automation tools.

## Key Functionality:

*   **Sandbox Lifecycle Management**: Offers REST APIs for:
    *   **Sandbox Definitions**: Managing the blueprints and configurations for different types of sandboxes.
    *   **Sandbox Pools**: Creating and managing groups of pre-configured sandboxes, enabling rapid deployment for training sessions.
    *   **Individual Sandboxes**: Handling the provisioning, starting, stopping, resetting, and tearing down of specific sandbox instances.
*   **Cloud Provider Integration**: While the `README.md` specifically mentions "manipulation of OpenStack cloud platform," the service is designed to be cloud-agnostic. It leverages dedicated drivers (like `backend-aws-lib` and `backend-openstack-lib`) to interact with various cloud providers (OpenStack, AWS) to provision the necessary virtual infrastructure.
*   **Ansible Integration**: Provides functionality for "applying Ansible playbooks on sandbox machines," likely by interacting with an Ansible execution engine (potentially `backend-ansible-runner`) to configure and customize sandbox environments after provisioning.
*   **Modular Django Application**: Structured as a Django project with distinct applications for different concerns:
    *   `Sandbox Common Lib`: Shared functionalities used across the service.
    *   `Sandbox Definition App`: Manages the definitions and templates for sandboxes.
    *   `Sandbox Ansible App`: Handles the execution of Ansible automation tasks on sandboxes.
    *   `Sandbox Instance App`: Oversees the instantiation and management of active sandbox environments.
*   **Infrastructure as Code (IaC) Integration**: The mention of OpenStack Heat manipulation in `backend-openstack-lib` and the presence of a `tofu` directory (potentially hinting at OpenTofu/Terraform) suggests that this service drives IaC tools to provision cloud resources.
*   **Containerized Deployment**: Designed for Docker deployment, enabling scalability and ease of management within a microservices architecture. Includes details on image building and administrative access.

## Role in CyberRangeCZ:

The `backend-sandbox-service` is the central nervous system for the CyberRangeCZ platform's training environments:

*   **Automated Environment Provisioning**: Automates the complex process of setting up isolated and realistic cybersecurity training scenarios, reducing manual overhead and ensuring consistency.
*   **Dynamic Resource Allocation**: Manages the dynamic allocation and deallocation of cloud resources, optimizing resource utilization and cost.
*   **Flexible Training Scenarios**: Supports a wide array of training scenarios by allowing instructors to define custom sandbox topologies, software installations, and network configurations.
*   **Platform Integration**: Provides the necessary APIs for the frontend and other backend services to request and manage sandbox environments, forming the backbone of the training platform.

This service is fundamental to the platform's ability to deliver scalable, dynamic, and effective hands-on cybersecurity training.
