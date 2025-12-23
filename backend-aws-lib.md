# backend-aws-lib

This repository contains `cyberrangecz-aws-lib`, a Python library specifically designed to act as an **AWS driver for the `sandbox-service` microservice** within the CyberRangeCZ platform. Its primary function is to abstract and facilitate programmatic interaction with Amazon Web Services (AWS) APIs, enabling the platform to provision, manage, and tear down sandbox environments in an AWS cloud infrastructure.

## Key Features:

*   **AWS Cloud Driver**: Provides a specialized driver for AWS, allowing the `sandbox-service` (a Django-based microservice) to interact with various AWS resources.
*   **`CyberrangeczCloudClientBase` Implementation**: Adheres to a common interface (`CyberrangeczCloudClientBase`), ensuring seamless integration and interchangeability with other cloud drivers (e.g., for OpenStack) within the CyberRangeCZ ecosystem. This promotes a consistent approach to cloud resource management.
*   **`Boto3` Integration**: Leverages `Boto3`, the official Amazon Web Services (AWS) SDK for Python, to communicate with AWS APIs. This ensures robust, up-to-date, and feature-rich interaction with AWS services.
*   **Installable Component**: Designed as an installable Python package, meaning it's intended to be imported and used by other applications (like `sandbox-service`) rather than being a standalone executable.

## Role in CyberRangeCZ:

The `backend-aws-lib` is a critical component for the CyberRangeCZ platform's multi-cloud capabilities:

*   **Enables AWS Backend**: Allows the platform to utilize AWS as a cloud provider for deploying and hosting cybersecurity training sandboxes.
*   **Abstraction Layer**: Provides a necessary abstraction over the complexities of direct AWS API calls, simplifying the development of cloud-agnostic sandbox management logic in the `sandbox-service`.
*   **Resource Provisioning**: Facilitates tasks such as launching virtual machines (EC2 instances), configuring networking (VPCs, subnets, security groups), and managing storage, all within AWS.

By providing a robust and integrated AWS driver, this library significantly contributes to the flexibility and scalability of the CyberRangeCZ platform, allowing it to offer training environments on a leading public cloud provider.
