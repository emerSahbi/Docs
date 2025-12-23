# backend-terraform-client

This repository contains `cyberrangecz-terraform-client`, a Python library designed to provide a programmatic interface for interacting with **Terraform (or its fork, OpenTofu)**. As a core component of the CyberRangeCZ platform's Infrastructure as Code (IaC) model, this client enables backend services to automate the provisioning, management, and de-provisioning of cloud infrastructure resources across various cloud providers (e.g., OpenStack, AWS).

## Key Features:

*   **Terraform/OpenTofu Automation**: Provides a Python API to execute Terraform/OpenTofu commands programmatically. This likely includes functions for:
    *   Initializing Terraform workspaces (`terraform init`).
    *   Generating and previewing execution plans (`terraform plan`).
    *   Applying configuration changes to provision or update infrastructure (`terraform apply`).
    *   Destroying provisioned infrastructure resources (`terraform destroy`).
    *   Managing Terraform state files.
    *   Passing and managing Terraform variables.
*   **Integration with Cloud Commons**: As noted in `backend-python-commons`, this client utilizes the `cloud_commons` module, indicating shared logic and interfaces for cloud-related operations, ensuring consistency across different cloud interactions.
*   **IaC Enablement**: Facilitates the platform's "infrastructure-as-code" approach, where infrastructure configurations are defined in declarative code and managed through version control.
*   **Python Library**: Designed as an installable Python package, intended to be consumed by other Python-based services (like `backend-sandbox-service` or `devops-tf-deployment`) that need to automate infrastructure changes.

## Role in CyberRangeCZ:

The `backend-terraform-client` is a crucial building block for the dynamic provisioning capabilities of the CyberRangeCZ platform:

*   **Automated Sandbox Deployment**: Enables the automatic setup of complex virtualized environments for training sandboxes, including virtual machines, networks, firewalls, and storage.
*   **Multi-Cloud Agnostic IaC**: Works in conjunction with cloud-specific drivers (like `backend-aws-lib` and `backend-openstack-lib`) to abstract the underlying cloud provider, allowing for consistent IaC practices across different cloud environments.
*   **Reproducibility and Consistency**: Ensures that sandbox environments are provisioned consistently and reproducibly, which is essential for fair and effective training.
*   **Scalability**: Allows the platform to scale its infrastructure provisioning capabilities by automating repetitive and complex tasks.

This library is fundamental to how the CyberRangeCZ platform efficiently and reliably deploys and manages its dynamic cloud infrastructure for cybersecurity training.
