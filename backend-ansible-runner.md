# backend-ansible-runner

Despite its name, this repository (primarily driven by the `manage_answers.py` script) serves a specialized function within the CyberRangeCZ platform, focusing on the **generation and management of dynamic "answers" or configurations for sandbox environments**. While it operates within an ecosystem that utilizes Ansible (evidenced by its consumption of Ansible inventory variables), its core task is not to execute Ansible playbooks directly but rather to interact with a dedicated "answers storage" microservice.

## Key Functionality:

*   **Dynamic Answer Generation**: The `manage_answers.py` script generates sandbox-specific "answers" or dynamic configurations. These answers are derived from a `variables.yml` file and a deterministic `seed` value, which is in turn generated from sandbox identification parameters (`global_pool_id`, `global_sandbox_id`, `global_sandbox_allocation_unit_id`). This allows for randomized yet repeatable generation of unique data for each sandbox.
*   **Interaction with Answers Storage**: It acts as a client to a separate `backend-answers-storage` microservice:
    *   **`POST` Answers**: Uploads the newly generated answers for a specific sandbox to the `answers-storage` service.
    *   **`DELETE` Answers**: Provides functionality to remove existing answers from the `answers-storage` service for cleanup purposes.
*   **Local Storage of Answers**: Before being sent to the `answers-storage` service, the generated answers are also saved locally to a specified file.
*   **Containerized Execution**: The presence of a `Dockerfile` and `entrypoint.sh` indicates that this component is designed to run as a Docker container, making it easily deployable and manageable within the platform's microservices architecture. The `entrypoint.sh` likely executes the `manage_answers.py` script, passing necessary parameters.
*   **Input Requirements**: Expects an Ansible `inventory.ini` file (to extract sandbox IDs), a local path for generated answers, and the URL of the `answers-storage` API.

## Role in CyberRangeCZ:

This `backend-ansible-runner` component is crucial for creating dynamic and interactive training scenarios:

*   **Personalized Training**: Enables the generation of unique solutions or data sets for each trainee's sandbox, preventing direct copying and promoting genuine problem-solving.
*   **Automated Solution Delivery**: Allows solutions or critical information (e.g., credentials, flags) to be dynamically generated and made available to other services or directly to trainees as part of the exercise flow.
*   **Testing and Validation**: Provides a mechanism to generate expected outcomes for automated validation of trainee actions.

In essence, this service acts as an intelligent intermediary, bridging the gap between dynamic sandbox provisioning and the unique data required to drive personalized and effective cybersecurity training.
