# frontend-visualization-dashboard

This repository contains an Angular library that provides a dashboard component for visualizing training data within the CyberRangeCZ platform. It is designed to be a reusable component that can be embedded in other applications. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-visualization-dashboard` library provides a single Angular component, `<crczp-dashboard>`, that serves as a container for various training data visualizations.

*   **Dashboard Component**: The library's main feature is the `<crczp-dashboard>` component, which takes the following inputs:
    *   `trainingInstanceId`: The ID of the training instance to visualize.
    *   `trainingDefinitionId`: The ID of the training definition.
    *   `hasReferenceSolution`: A boolean indicating whether a reference solution is available for display.

*   **Integration of Visualizations**: The dashboard component integrates and orchestrates several other visualization components, such as:
    *   A clustering visualization to group trainees based on their behavior.
    *   A timeline visualization to show the sequence of events in a training run.
    *   A hurdling visualization to compare the progress of different trainees.

*   **Interactive Filtering and Highlighting**: The dashboard allows for interactive filtering and highlighting of trainees. These interactions are synchronized across all the integrated visualizations, providing a cohesive and unified user experience.

*   **Data Service**: The dashboard uses a `VisualizationsDataService` to fetch the data for the visualizations from the backend.

## Role in CyberRangeCZ:

The `frontend-visualization-dashboard` library provides a powerful tool for instructors and administrators to monitor and analyze training sessions. It enables them to:

*   Get a high-level overview of a training instance.
*   Drill down into the details of individual trainee performance.
*   Compare the performance of different trainees.
*   Identify patterns and trends in trainee behavior.

By providing a rich and interactive set of visualizations, this library enhances the training experience and provides valuable insights into the learning process.
