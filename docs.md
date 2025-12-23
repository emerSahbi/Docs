# docs

This repository contains the **source code and configurations for the official CyberRangeCZ Platform documentation website**. It leverages MkDocs, a static site generator, to transform Markdown-formatted documentation files into a professional, navigable, and easily deployable static website.

## Key Technologies and Features:

*   **MkDocs**: The core tool used for building the documentation. MkDocs allows documentation to be written in Markdown, which is then compiled into a static HTML site.
*   **Python-based**: Requires Python 3.10 and `pipenv` for dependency management, making the documentation generation process consistent and reproducible.
*   **Structured Documentation**: The documentation content resides in the `docs` subdirectory, organized into Markdown files that reflect the structure of the documentation website.
*   **Customization**: The `overrides` directory likely contains custom templates, CSS, or JavaScript to tailor the appearance and functionality of the MkDocs theme, ensuring the documentation aligns with the CyberRangeCZ branding and user experience.
*   **Static Site Generation**: The `site` directory, once generated, contains the complete static HTML, CSS, and JavaScript files that can be hosted on any web server or platform (e.g., GitHub Pages).
*   **Local Development Server**: Provides easy-to-use commands (`pipenv run mkdocs serve`) to run a local development server, allowing authors to preview changes to the documentation in real-time.
*   **GitHub Pages Deployment**: The documentation is deployed to GitHub Pages, making it publicly accessible at `https://cyberrangecz.github.io/docs/`.

## Role in CyberRangeCZ:

The `docs` repository is critical for the usability, maintainability, and adoption of the CyberRangeCZ platform:

*   **Centralized Information Hub**: Serves as the primary source of truth for all information related to the CyberRangeCZ platform, including user guides, developer documentation, installation instructions, and architectural overviews.
*   **User Empowerment**: Provides users (trainees, instructors, administrators) with the necessary information to effectively use and interact with the platform.
*   **Developer Onboarding**: Offers comprehensive documentation for developers working on the platform, facilitating understanding of its architecture, APIs, and development workflows.
*   **Content Creation Support**: By using Markdown and MkDocs, it simplifies the process for contributors to write and update documentation.
*   **Versioned Documentation**: Allows for versioning of documentation alongside the code, ensuring that users can access documentation relevant to specific versions of the platform.

This repository is essential for disseminating knowledge about the CyberRangeCZ platform, ensuring that all stakeholders have access to the information they need to succeed.
