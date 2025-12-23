# docker-image-builder

This repository defines a specialized Docker image that bundles a collection of essential tools for **building and provisioning virtual machine images and managing infrastructure as code**. This image is a critical component for automating the creation and customization of the base VM images and the underlying infrastructure used within the CyberRangeCZ platform.

## Key Tools Included in the Docker Image:

*   **QEMU**: A versatile machine emulator and virtualizer. It's used to run and manage virtual machines, often as part of the image build process.
*   **Packer**: A tool by HashiCorp for creating identical machine images from a single source configuration for multiple platforms (e.g., KVM, AWS, OpenStack). Packer uses builders (like QEMU) and provisioners (like Ansible) to create these images.
*   **Ansible**: An automation engine used for configuration management, application deployment, and orchestrating more advanced provisioning tasks within the virtual machine images.
*   **OpenTofu**: An open-source fork of Terraform, an Infrastructure as Code (IaC) tool. OpenTofu is used to define, provision, and manage cloud and on-premises resources.

## Key Functionality and Use Cases:

*   **Automated VM Image Creation**: The bundled tools enable a fully automated pipeline for creating standardized virtual machine images, which are then used as base operating systems for CyberRangeCZ sandboxes.
*   **Infrastructure Provisioning**: Facilitates the provisioning and management of the underlying infrastructure required for sandboxes (e.g., virtual machines, networks, storage) using OpenTofu.
*   **Customization and Configuration**: Ansible is used to customize and configure the operating system and installed software within the VM images during the Packer build process.
*   **Consistent Build Environment**: Provides a consistent and isolated environment (a Docker container) for running image building and infrastructure provisioning tasks, ensuring reproducibility and reducing "works on my machine" issues.
*   **Privileged Execution**: The example usage shows the container running in `--privileged` mode with `--network=host`, indicating that it needs elevated permissions and direct network access to interact with host-level virtualization technologies (like KVM/libvirt) for creating/managing VMs.

## Role in CyberRangeCZ:

This `docker-image-builder` is fundamental to the scalability and consistency of the CyberRangeCZ platform. It empowers the platform to:

*   **Rapidly Generate Base Images**: Quickly create and update diverse VM images (e.g., image-kali, image-windows-10, image-debian) tailored for specific training scenarios.
*   **Automate Infrastructure Deployment**: Streamline the provisioning of complex virtualized infrastructure required for dynamic sandbox environments.
*   **Maintain Version Control of Images**: Ensure that all VM images used in the platform are built from a version-controlled definition, allowing for easy updates and rollbacks.

By centralizing the tools needed for image building and IaC, this repository contributes to the overall automation and maintainability of the CyberRangeCZ's foundational infrastructure.
