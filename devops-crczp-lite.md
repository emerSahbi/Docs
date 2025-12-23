# devops-crczp-lite

This repository provides a **lightweight and self-contained deployment solution for the CyberRangeCZ Platform**, primarily aimed at facilitating evaluation, local development, and content creation. It is explicitly noted as *not* suitable for production workloads due to resource constraints and the overhead of nested virtualization.

## Key Functionality:

*   **Single-Host Deployment**: Designed to deploy a complete (albeit scaled-down) CyberRangeCZ platform onto a single host machine.
*   **Nested Virtualization**: Achieves this by first deploying an OpenStack cloud environment within a single KVM virtual machine, and then setting up the CyberRangeCZ Platform services inside that OpenStack instance. This "double to triple virtualization" is why it's not recommended for performance-critical production use.
*   **Vagrant Integration**: Utilizes Vagrant (specifically with the `vagrant-libvirt` provider for KVM) to automate the provisioning of the base KVM VM and initiate the deployment process.
*   **Ansible Integration**: The presence of `ansible.cfg` indicates that Ansible is used for configuration and provisioning within the Vagrant-managed VM.
*   **Google Cloud Platform (GCP) Support**: Includes sample Terraform code (`tf-gcp-vm`) to provision a suitable virtual machine on GCP, demonstrating how to host the `crczp-lite` environment in a public cloud.
*   **Access Details**: Provides clear instructions and default credentials for accessing the deployed OpenStack API/GUI (Horizon) and the underlying KVM environment, making it easy for users to interact with the installed platform.

## Role in CyberRangeCZ:

The `devops-crczp-lite` repository is invaluable for various use cases within the CyberRangeCZ ecosystem:

*   **Rapid Evaluation**: Allows potential users or stakeholders to quickly spin up a functional instance of the platform for testing and review without needing a full-scale production environment.
*   **Content Creation**: Provides content developers (e.g., for training scenarios, virtual machine images) with a local and isolated environment to test their creations without affecting live deployments.
*   **Local Development**: Offers a convenient setup for developers to work on CyberRangeCZ components, replicate issues, and test changes in a consistent environment.
*   **Demonstration**: Useful for demonstrating the platform's capabilities in a resource-efficient manner.

This solution democratizes access to the CyberRangeCZ platform, making it accessible for a broader range of users for development and evaluation purposes.
