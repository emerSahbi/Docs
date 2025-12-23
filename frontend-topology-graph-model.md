# frontend-topology-graph-model

**Note: The code from this repository has been integrated into the [frontend-platform monorepo](https://github.com/cyberrangecz/frontend-platform), where its development and maintenance are now continued.**

This repository previously contained the **"Topology Graph Model"**, an Angular (TypeScript) library specifically dedicated to defining the **data models (interfaces and classes) for representing network topologies as graphs**. Its primary purpose was to provide a standardized, type-safe, and D3.js-compatible structure for topology data, essential for frontend visualization components like `frontend-topology-graph`.

## Historical Functionality:

*   **Network Element Models**: Defined TypeScript interfaces and classes for various elements commonly found in network topologies, including:
    *   `Node`: An abstract or base type for network devices, with concrete implementations like `SwitchNode`, `HostNode`, `RouterNode`, and `SpecialNode`.
    *   `Node Port`: Represents connection points on network nodes.
    *   `Link`: Defines the connections between nodes.
    *   Related `Enums`: For types or states of topology elements.
*   **D3.js Compatibility**: Explicitly designed to extend D3.js `Node` and `Link` models, ensuring seamless integration with D3.js-based visualization libraries. This made it easier to render complex network diagrams.
*   **Type Safety**: Leveraging TypeScript, the library ensured that all frontend components manipulating or displaying topology data did so with strong type checking, reducing potential runtime errors.
*   **Consistency**: Provided a common language and structure for topology data across the frontend, preventing redundant or inconsistent data model definitions.

## Technologies Used:

*   **Angular / TypeScript**: Utilizing TypeScript's strong typing features to define clear and robust data structures.
*   **D3.js**: Ensuring compatibility with the widely used data visualization library.
*   **NPM/Node.js**: For dependency management and project tooling.

## Role in CyberRangeCZ (Historical Context):

Historically, the `frontend-topology-graph-model` library was fundamental for the reliable and efficient development of network topology visualizations within the CyberRangeCZ platform:

*   **Foundation for Visualizations**: Provided the essential data structures that `frontend-topology-graph` and other visualization components used to process and render network topologies.
*   **Improved Development Experience**: Simplified the development of topology-related features by offering ready-to-use, type-safe models, allowing developers to focus on the visualization logic.
*   **Ensured Data Integrity**: By enforcing a consistent data model, it helped ensure that topology data was correctly interpreted and displayed throughout the frontend.

Its integration into the `frontend-platform` monorepo signifies a consolidation of all frontend data model libraries into a single `libs/model` structure. This centralizes the platform's understanding of its core data entities, enhancing overall development efficiency and maintainability.
