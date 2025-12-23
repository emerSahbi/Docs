# frontend-hurdling-visualization

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained an **Angular-based frontend component designed for the visualization of "hurdling" within training runs** in the CyberRangeCZ platform. Its primary goal was to provide instructors with a comprehensive and real-time overview of trainee progress through training levels, enabling them to monitor the ongoing course of training, identify delays, and explore individual trainee walkthroughs.

## Historical Functionality:

*   **Trainee Progress Visualization**: Presents training data with rows representing individual trainees and bars representing training levels.
*   **Color-Coded Progress**:
    *   Gray bars indicate completed levels.
    *   Colored bars (green/yellow/red) denote current levels, with colors signifying delay or adherence to scheduled time.
    *   Stripped bars represent scheduled time for ongoing or upcoming levels.
*   **Instructor-Centric View**: Designed to give instructors a full picture of a trainee's journey through a training module, allowing for filtering and detailed inspection of selected trainees.
*   **Identification of Delays/Outliers**: The visual cues for delays (yellow/red bars) help instructors quickly identify trainees who might be struggling or falling behind.
*   **Simulated Data Support**: Includes features for simulating training runs with provided test data, useful for development and testing of the visualization itself.
*   **Integration with Backend**: Relied on data from the `backend-training` service to fetch training run information.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, this "hurdling" visualization component was crucial for the real-time monitoring and management of training sessions by instructors. It provided:

*   **Real-time Oversight**: Allowed instructors to observe trainee progress as it unfolded, facilitating timely intervention or support.
*   **Performance Analysis**: Enabled instructors to analyze how different trainees navigate the same training, identifying patterns and individual learning paces.
*   **Adaptive Training Insights**: For adaptive training scenarios, it would help in understanding how trainees adapted to challenges and how the system guided them.

Its integration into the `frontend-platform` monorepo signifies a consolidation of frontend assets, aiming for a more cohesive and efficiently managed user interface for the entire platform's analytical and monitoring capabilities.
