# frontend-training-agenda

This repository contains a suite of Angular libraries that provide the user interface components and services for managing training within the CyberRangeCZ platform. It functions as the frontend for the `backend-training` and related microservices. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-training-agenda` is a monorepo that contains a collection of libraries, each dedicated to a specific feature of the training management lifecycle. This modular architecture allows consuming applications to import only the features they need.

The main features are categorized as follows:

*   **Training Definition**: Libraries for creating, viewing, and managing the templates for training exercises.
    *   `definition-overview`: A high-level view of all available training definitions.
    *   `definition-edit`: Components for creating and modifying training definitions.
    *   `definition-detail`: A detailed view of a single training definition.
    *   `definition-preview`: A feature to preview a training definition before it is used.

*   **Training Instance**: Libraries for managing specific instances of a training definition.
    *   `instance-overview`: An overview of all training instances.
    *   `instance-edit`: Components for creating and configuring training instances.
    *   `instance-detail`: A detailed view of a single training instance.
    *   `instance-runs`: A view of all the times a training instance has been run.
    *   `instance-progress`: Components to track the progress of an ongoing training instance.
    *   `instance-results`: A view of the results and outcomes of a completed training instance.

*   **Training Run**: Libraries for the actual execution of a training instance.
    *   `run-overview`: A list of all training runs.
    *   `run-detail`: A detailed view of a specific training run, possibly showing user interactions and events.
    *   `run-results`: A view of the results of a training run.

*   **Adaptive Training**: A parallel set of libraries for "adaptive" training, which likely involves scenarios that change dynamically based on the user's actions. These libraries mirror the structure of the standard training features.

*   **Cheating Detection**: A set of libraries for identifying and managing cheating in training instances.

*   **MITRE Techniques**: Integration with the MITRE ATT&CK framework, allowing for the association of training exercises with specific tactics and techniques.

## Role in CyberRangeCZ:

The `frontend-training-agenda` provides the complete user interface for the training lifecycle in the CyberRangeCZ platform. It enables:

*   **Training Authors**: To design and build complex training scenarios.
*   **Instructors**: To manage and monitor training instances.
*   **Trainees**: To participate in and interact with training exercises.
*   **Administrators**: To get an overview of all training activities.

By providing a rich set of reusable components and services, this repository ensures a consistent and user-friendly experience across all training-related activities in the platform.
