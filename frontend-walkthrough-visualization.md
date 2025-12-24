# frontend-walkthrough-visualization

This repository contains an Angular library that provides a Sankey diagram visualization for training walkthroughs within the CyberRangeCZ platform. It is designed to be a reusable component that can be embedded in other applications. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-walkthrough-visualization` library provides a single Angular component, `<crczp-walkthrough-visualization>`, that visualizes the paths trainees take through a training exercise.

*   **Sankey Diagram Visualization**: The library's main feature is the `<crczp-walkthrough-visualization>` component, which renders a Sankey diagram. This type of diagram is used to show flows and their quantities, making it ideal for visualizing how trainees move between different stages of a training exercise.

*   **Inputs**: The component takes the following inputs:
    *   `instanceId`: The ID of the training instance to visualize.
    *   `levels`: An array of the levels in the training exercise.

*   **Level Selection**: The component allows the user to select a specific level and view the corresponding walkthrough visualization for that level.

*   **Data Service**: The component uses a `WalkthroughVisualizationService` to fetch the data for the visualization from the backend.

## Role in CyberRangeCZ:

The `frontend-walkthrough-visualization` library provides a valuable tool for instructors and training designers to understand how trainees are interacting with the training content. It can be used to:

*   Identify common paths that trainees take through an exercise.
*   Find bottlenecks or areas where trainees are struggling.
*   Compare the paths of different trainees.

By providing a clear and intuitive visualization of the training flow, this library helps to improve the design and effectiveness of the training exercises.
