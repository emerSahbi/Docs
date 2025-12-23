# frontend-clustering-visualization

**Note: The code from this repository has been integrated into the `frontend-platform` monorepo, where its development and maintenance are now continued.**

This repository previously contained an **Angular-based frontend component dedicated to the visualization of trainee behavior clustering** within the CyberRangeCZ platform. Its primary goal was to provide analytical views into collected training data, specifically focusing on features that define how trainees interact with the exercises, allowing instructors and researchers to identify outliers or distinct strategies employed by participants during their gameplay.

## Historical Functionality:

*   **Trainee Behavior Analysis**: Processed collected data to highlight patterns and groups within trainee actions.
*   **Outlier Detection**: Helped in identifying unusual or exceptional trainee behaviors that deviate from the norm.
*   **Strategy Exploration**: Enabled the exploration of different strategies adopted by trainees, providing insights into various problem-solving approaches.
*   **Multiple Views**: Offered three distinct views for processing and presenting the clustered data, catering to different analytical needs.
*   **Integration with Backend**: Relied on data from the `backend-training` service and user information from the `backend-user-and-group` service to function.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, this clustering visualization component was a powerful tool for enhancing the analytical capabilities of the CyberRangeCZ platform. It provided:

*   **Deeper Pedagogical Insights**: Helped instructors understand trainee learning processes at a more granular level, moving beyond simple pass/fail metrics.
*   **Content and Scenario Refinement**: Insights gained from clustering could inform improvements to training content and scenario design.
*   **Research and Development**: Served as a valuable component for researchers studying learning patterns in cybersecurity education.

Its integration into the `frontend-platform` monorepo represents a consolidation of frontend assets, aiming for a more cohesive and efficiently managed user interface for the entire platform.
