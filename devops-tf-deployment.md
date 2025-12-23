# devops-tf-deployment

This repository is a critical component of the CyberRangeCZ platform's DevOps strategy, providing the **Infrastructure as Code (IaC) tools and configurations for deploying the entire platform to both OpenStack and AWS cloud environments using OpenTofu** (a Terraform fork). It orchestrates the provisioning of the foundational cloud infrastructure that hosts the Kubernetes clusters where the CyberRangeCZ microservices (deployed by `devops-helm`) will ultimately run.

## Key Functionality and Components:

*   **Multi-Cloud Provisioning**: Supports deploying the CyberRangeCZ platform on:
    *   **OpenStack**: Utilizes `tf-openstack-base` for provisioning base resources, with specific requirements for Nova, Neutron, Keystone, floating IPs, and internet-connected routers.
    *   **AWS**: Employs `tf-aws-base` and `tf-aws-kube-base` for AWS resource provisioning, including considerations for VPC limits and sandbox topology definitions.
*   **OpenTofu-driven**: Leverages OpenTofu (a compatible alternative to Terraform) for declarative infrastructure management, ensuring consistency and version control of cloud resources.
*   **Two-Step Deployment Process**:
    1.  **Base Cloud Resource Deployment**: Provisioning of fundamental cloud infrastructure, such as compute flavors, VM images, networking (VPCs, subnets, security groups), and instances. This is handled by `tf-openstack-base` for OpenStack or `tf-aws-base` and `tf-aws-kube-base` for AWS.
    2.  **Helm Application Deployment**: Once the base infrastructure is ready, `tf-head-services` is used to deploy the CyberRangeCZ Platform's Helm application (from `devops-helm`) onto the newly provisioned virtual infrastructure.
*   **Detailed Documentation**: Provides links to internal markdown files (`BASE.md`, `HELM.md`) for step-by-step deployment instructions, ensuring a guided and repeatable process.
*   **Modular Terraform Configurations**: The repository is structured with modular Terraform configurations (`tf-aws-base`, `tf-aws-kube-base`, `tf-head-services`, `tf-openstack-base`) to manage different aspects of the infrastructure deployment.

## Role in CyberRangeCZ:

The `devops-tf-deployment` repository is foundational for the operational deployment of the CyberRangeCZ platform:

*   **Automated Infrastructure Provisioning**: Automates the complex and error-prone process of setting up cloud infrastructure, ensuring that environments are consistently configured.
*   **Cloud Agnostic Orchestration**: Provides a unified IaC approach across different cloud providers, allowing the platform to be deployed flexibly based on organizational needs or resource availability.
*   **Reproducible Environments**: Guarantees that production and testing environments can be spun up identically, crucial for reliability and debugging.
*   **Scalability**: Enables the platform to scale its infrastructure footprint by automating resource allocation and management.
*   **Integration with Kubernetes Deployment**: Acts as the first step in a two-phase deployment, setting up the foundation before the Kubernetes-native components are deployed via Helm.

This repository empowers the CyberRangeCZ platform to deploy its sophisticated training environments with high efficiency, consistency, and reliability across leading cloud infrastructures.
