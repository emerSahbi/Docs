# devops-helm

This repository serves as the **primary tool for deploying the entire CyberRangeCZ platform onto Kubernetes clusters using Helm**. It contains a comprehensive collection of Helm charts and configuration files that define, install, and manage the various microservices and infrastructure components of the platform. Beyond just deployment, it also outlines a local development and testing environment using Vagrant that integrates with cloud resources.

## Key Components and Functionality:

*   **Helm Charts (`helm` directory)**: Contains individual Helm charts for different parts of the CyberRangeCZ platform, including:
    *   `crczp-certs`: Likely manages TLS certificates for secure communication within the cluster.
    *   `crczp-gen-users`: Potentially handles the generation or initial provisioning of users within the Kubernetes environment.
    *   `crczp-head`: The main Helm chart for deploying the core CyberRangeCZ application or its central control plane.
    *   `crczp-postgres`: A Helm chart for deploying and managing a PostgreSQL database instance, used by many backend services.
*   **Kubernetes Deployment**: Automates the deployment of all necessary CyberRangeCZ microservices, databases, and supporting infrastructure onto a Kubernetes cluster.
*   **Vagrant Integration for Local Development**:
    *   Includes a `Vagrantfile` and `vagrant-values.yaml-template` to set up a local development or testing environment.
    *   This setup provisions a Vagrant VM that hosts the Kubernetes cluster.
    *   **Cloud Connectivity**: The local Vagrant environment is configured to interact with an external OpenStack cloud, from which the Kubernetes cluster's underlying VMs are provisioned. It also requires access to a `Proxy Jump host` VM.
*   **Training Definitions**: The `training-definitions` directory contains demo Linear and Adaptive Training Definitions, which are likely designed to be uploaded to the deployed platform to provide initial training content.
*   **Traffic Management**: Includes `traefik-config.yaml`, suggesting the use of Traefik as an Ingress Controller or load balancer within the Kubernetes cluster.
*   **Configuration Management**: Uses `values.yaml` for default Helm chart values and `vagrant-values.yaml-template` for customizing deployments in the Vagrant environment.

## Role in CyberRangeCZ:

The `devops-helm` repository is absolutely central to the operational aspects of the CyberRangeCZ platform:

*   **Standardized Deployment**: Ensures consistent, repeatable, and automated deployment of the complex microservice architecture onto Kubernetes.
*   **Environment Management**: Facilitates the management of both production-like Kubernetes deployments and local development/testing environments that mimic the production setup.
*   **Scalability and Resilience**: Leverages Kubernetes' features for container orchestration, scaling, and self-healing for the CyberRangeCZ components.
*   **Cloud Agnostic Orchestration**: By deploying onto Kubernetes, it abstracts the underlying cloud infrastructure (even when VMs are from OpenStack), allowing the platform to run on any Kubernetes-compatible cloud.
*   **Content Provisioning**: Provides a mechanism to upload initial training content and configurations after the platform is deployed.

This repository is the backbone of the CyberRangeCZ deployment strategy, making the platform's complex architecture manageable and deployable across various environments.
