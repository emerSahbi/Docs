# frontend-overview-visualization

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained an **Angular-based frontend component that provided comprehensive overview visualizations for training runs** within the CyberRangeCZ platform. Its primary goal was to offer instructors and administrators a high-level, aggregated view of training progress and trainee behavior, consolidating key metrics into interactive visual components.

## Historical Functionality:

This component comprised three independent Angular visualization components that could be used together or separately:

1.  **Overview Table (`crczp-visualization-overview-table`)**: Presented a summary table of training run data, offering a structured way to review key information about participants and their performance.
2.  **Clustering Visualization (`crczp-visualization-overview-clustering`)**: Displayed clusters of trainee data, likely to identify groups with similar behaviors or performance patterns (similar to the functionality of `frontend-clustering-visualization`).
3.  **Timeline Visualization (`crczp-visualization-overview-timeline`)**: Illustrated events or progress over time during a training run, allowing for a temporal analysis of trainee actions and milestones.

*   **Customizable Inputs**: Each component supported various input parameters for flexibility, including:
    *   `useLocalMock`: For using local JSON data for testing and development.
    *   `enableAllPlayers`: To show all participants or focus on a specific learner.
    *   `feedbackLearnerId`: To highlight a particular trainee in the visualizations.
    *   `colorScheme`: To customize the visual appearance.
    *   `size`: To control the dimensions of the visualization.
*   **Integration with Backend**: Relied on data from the `backend-training` service and user information from the `backend-user-and-group` service to fetch and display relevant training data.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, this overview visualization component was critical for providing high-level analytical insights to instructors and administrators of the CyberRangeCZ platform. It enabled them to:

*   **Quickly Gauge Training Status**: Obtain a rapid overview of active training sessions, participant engagement, and overall progress.
*   **Identify Trends and Patterns**: Detect overarching trends in trainee performance or behavior across multiple training runs.
*   **Facilitate Strategic Planning**: Use aggregated data to make informed decisions about curriculum development, resource allocation, and platform improvements.

Its integration into the `frontend-platform` monorepo signifies a strategic consolidation of frontend development, aiming for a more unified and efficiently managed user interface that provides a cohesive dashboard experience for the platform's various visualization capabilities.
