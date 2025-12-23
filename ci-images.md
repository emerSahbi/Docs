# ci-images

This repository serves as a centralized location for **GitHub Actions workflows and example configurations dedicated to the Continuous Integration (CI) and Continuous Delivery (CD) of virtual machine (VM) images** used within the CyberRangeCZ platform. Rather than directly storing the VM images, it provides the automation framework (the "how-to") for building, testing, and releasing these images.

## Key Components and Functionality:

*   **GitHub Actions Workflows (`.github/workflows`)**:
    *   `cleanup.yml`: Likely responsible for cleaning up old build artifacts, Docker images, or temporary resources associated with the CI process.
    *   `release.yml`: Orchestrates the release process for new versions of VM images. This would typically involve building the image, tagging it with a version, and pushing it to an artifact repository.
    *   `test.yml`: Defines the testing procedures for VM images, ensuring that newly built images meet quality standards and functional requirements.
*   **Image CI Example (`examples/image`)**: Provides a template structure that individual VM image repositories (like `image-kali` or `image-windows-10`) can copy and adapt to implement their own CI/CD pipelines. This example includes:
    *   **Terraform Configuration (`terraform.tf`, `terraform.tfvars`)**: Defines the infrastructure required to build or test a VM image. This could include provisioning a build server, network resources, or temporary VMs in a cloud environment.
    *   **Topology Definition (`topology.yml`)**: Specifies the virtual machine topology for the image build/test process, outlining the VMs, networks, and their configurations.
    *   **Provisioning Scripts (`provisioning` directory)**: Likely contains Ansible playbooks or other scripts used to customize the base VM image (install software, configure settings, etc.).

## Role in CyberRangeCZ:

The `ci-images` repository is fundamental to maintaining a high-quality and up-to-date collection of VM images for the CyberRangeCZ training environments:

*   **Automated Image Building**: Automates the complex process of creating new VM images, ensuring consistency and reducing manual errors.
*   **Quality Assurance**: Integrates testing into the image build process, verifying that images are functional, secure, and meet the platform's standards before being deployed into sandboxes.
*   **Version Control for Images**: By managing the CI/CD process for images, it effectively provides version control and traceability for all VM images used in the platform.
*   **Scalability and Efficiency**: Enables the rapid creation and update of diverse VM images required for a wide range of training scenarios, supporting the platform's scalability needs.

In essence, this repository provides the blueprint and automation tools for how the CyberRangeCZ platform consistently delivers the foundational virtual machine images that power its cybersecurity training sandboxes.
