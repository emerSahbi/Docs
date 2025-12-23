# ansible-role-guacamole

This repository contains an Ansible role for deploying Apache Guacamole to a Kubernetes cluster. Apache Guacamole is a clientless remote desktop gateway that provides access to desktops and servers using only a web browser, supporting protocols like VNC, RDP, and SSH.

This role is crucial for the CyberRangeCZ platform as it likely provides browser-based access to the virtual machines and environments created for cybersecurity training.

## Key Features:

*   **Helm-based Deployment**: The role utilizes a Helm chart, packaged within its `files` directory (`files/guacd`), to deploy the Apache Guacamole components. Helm simplifies the deployment and management of Kubernetes applications.
*   **Kubernetes Integration**: It is specifically designed to deploy Guacamole onto a Kubernetes cluster, making use of the `kubernetes.core.helm` Ansible module.
*   **K3s Compatibility**: The role targets `k3s` clusters, as indicated by its reliance on the `/etc/rancher/k3s/k3s.yaml` kubeconfig file.
*   **Namespace Management**: It deploys Guacamole into a dedicated `guacd` namespace, which is created by the role if it doesn't already exist.

This role centralizes the deployment of a critical access component for the CyberRangeCZ platform, enabling users to interact with their training environments securely through a web browser.
