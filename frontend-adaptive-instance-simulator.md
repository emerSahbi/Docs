# frontend-adaptive-instance-simulator

**Note: The code from this repository has been integrated into the `frontend-platform` monorepo, where its development and maintenance are now continued.**

This repository previously contained the **"Adaptive Model Simulator"**, an Angular-based frontend application. Its primary purpose was to provide a tool for **simulating and visualizing adaptive training runs** within the CyberRangeCZ platform. This simulator allowed developers, instructors, and content creators to predict the behavior of adaptive training paths based on various factors and to visualize the dynamics of training runs and task difficulties.

## Historical Functionality:

*   **Adaptive Training Simulation**: Enabled the simulation of how an adaptive training exercise would progress under different conditions or with varying trainee inputs.
*   **Visualization of Training Dynamics**: Provided visual representations of the training runs, illustrating how factors influence the adaptive model and how task difficulties evolve throughout an exercise.
*   **Debugging and Testing Adaptive Logic**: Served as a crucial tool for understanding, debugging, and testing the complex algorithms and logic implemented in backend adaptive training services (e.g., `backend-adaptive-training`).
*   **Content Creation Support**: Helped content creators design and validate adaptive training scenarios by allowing them to preview the adaptive behavior.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **NPM/Node.js**: For dependency management and project tooling.
*   **Integration with Backend**: Designed to interact with the `backend-adaptive-training` service to fetch data and apply adaptive logic.

## Role in CyberRangeCZ (Historical Context):

Historically, this simulator was vital for the development and refinement of the adaptive training capabilities of the CyberRangeCZ platform. It provided a sandbox environment for working with the adaptive model without requiring a full-scale deployment of all backend services. Its integration into the `frontend-platform` monorepo signifies a consolidation of frontend development efforts, centralizing various frontend applications into a single, cohesive codebase.
