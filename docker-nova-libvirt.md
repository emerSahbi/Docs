# docker-nova-libvirt

This repository, despite its `docker-` prefix, primarily appears to provide **configuration templates for integrating OpenStack Nova (the compute service) with Libvirt** within the CyberRangeCZ platform's deployment ecosystem. The absence of a Dockerfile in the root directory suggests it doesn't build a Docker image directly, but rather offers resources for systems that involve Docker in their Nova/Libvirt setup or configuration.

## Key Components and Functionality:

*   **`template-overrides.j2`**: This Jinja2 template is the central piece of this repository. Jinja2 templates are typically used by Ansible or similar configuration management tools to generate dynamic configuration files. In this context, it is highly probable that this template is used to:
    *   Configure OpenStack Nova to use Libvirt as its virtualization driver.
    *   Set specific parameters or overrides for Nova's interaction with the Libvirt hypervisor.
    *   Define how virtual machines managed by Nova are handled by the underlying Libvirt virtualization layer.
*   **Integration with OpenStack Deployments**: Given CyberRangeCZ's support for OpenStack as a cloud backend and its use of `devops-crczp-lite` (which sets up OpenStack within a KVM VM using Libvirt), this repository's templates are likely consumed by Ansible roles or deployment scripts responsible for configuring these OpenStack components.

## Role in CyberRangeCZ:

The `docker-nova-libvirt` repository contributes to the CyberRangeCZ platform by:

*   **Standardizing Nova/Libvirt Configuration**: Provides a consistent and reusable way to configure the Nova compute service to effectively utilize Libvirt-managed hypervisors.
*   **Enabling OpenStack on KVM**: Essential for deployments where OpenStack is running on KVM-based virtual machines (e.g., in nested virtualization scenarios for local development or within dedicated KVM hosts).
*   **Infrastructure Flexibility**: Supports the platform's ability to provision and manage virtual machines within OpenStack environments that rely on Libvirt for virtualization.

This repository, through its templated configurations, helps ensure the correct and efficient operation of the OpenStack compute layer, which is fundamental for hosting the dynamic training sandboxes.
