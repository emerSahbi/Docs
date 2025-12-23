# frontend-statistical-visualizations

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained an **Angular-based frontend component that provided a collection of graphs and visualizations for displaying and exploring statistical data from multiple training instances** within a single training definition in the CyberRangeCZ platform. Its primary goal was to offer instructors and administrators aggregated analytical insights into overall training effectiveness, trends, and patterns across various training runs.

## Historical Functionality:

*   **Aggregated Data Visualization**: Presents statistical summaries and trends derived from data collected across multiple training instances of the same definition.
*   **Exploratory Data Analysis**: Enabled users to explore and analyze consolidated training data, identifying overall performance trends, common difficulties, or areas of high success.
*   **Various Graphs and Visualizations**: Likely included different types of charts (e.g., bar charts, line graphs, pie charts) to represent various statistical metrics effectively.
*   **Integration with Backend**: Relied on data from the `backend-training` service (for training data) and the `backend-user-and-group` service (for user context) to retrieve the necessary information for its visualizations.

## Technologies Used:

*   **Angular**: A TypeScript-based open-source frontend web application framework.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, this statistical visualization component was critical for providing a macro-level view of training performance and analytics within the CyberRangeCZ platform. It enabled:

*   **Overall Training Effectiveness Assessment**: Helped evaluate the success of entire training programs or specific training definitions.
*   **Curriculum Development**: Provided data-driven insights that could inform improvements and adjustments to the training curriculum.
*   **Benchmarking**: Allowed for benchmarking performance across different cohorts or over time.

Its integration into the `frontend-platform` monorepo signifies a strategic consolidation of frontend assets, aiming for a more cohesive and efficiently managed user interface that provides a comprehensive suite of analytical and reporting tools for the platform.
