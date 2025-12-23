# backend-automated-problem-generation-lib

This repository contains a Python package designed to facilitate the **automated generation of random data within specified restrictions**. Named "generator library," it serves as a crucial backend component for creating dynamic and unique challenges, flags, or configuration values for individual players or sandbox instances within the CyberRangeCZ cybersecurity training platform.

## Key Features:

*   **Dynamic Data Generation**: Generates various types of random data based on predefined rules and constraints. This capability is vital for personalizing training scenarios and ensuring that each trainee receives unique challenge elements.
*   **Supported Variable Types**: The library supports the generation of several common data types:
    *   `username`: Produces randomly chosen usernames.
    *   `password`: Generates random character strings suitable for passwords.
    *   `port`: Creates random port numbers within a given range.
    *   `text`: Selects random sentences or text snippets.
    *   `IP`: Generates random IP addresses.
*   **Configurable Generation Parameters**: Users define desired data generation parameters through a YAML input file. For each variable, mandatory attributes like `type` are specified, along with optional attributes such as:
    *   `min` / `max`: For numerical ranges (e.g., ports, IPs).
    *   `length`: For string lengths (e.g., usernames, passwords).
    *   `prohibited`: A list of values to be excluded from generation.
    *   `challenge_id`: An identifier possibly used for linking generated values to specific challenges within a CTFd system.
*   **Core Components**: The package (`generator`) is structured with:
    *   `var_generator.py`: Implements the core logic for generating random values based on `Variable` objects.
    *   `var_parser.py`: Handles the parsing of input YAML files into `Variable` objects.
    *   `var_object.py`: Defines the `Variable` class, encapsulating all parameters for a single generated value.
*   **Integration with CTFd**: Explicitly designed to integrate with a "generator application" for CTFd, indicating its role in populating capture-the-flag exercises with dynamically created flags or challenge components.

## Role in CyberRangeCZ:

The `backend-automated-problem-generation-lib` is fundamental to creating a scalable and engaging training experience:

*   **Personalized Challenges**: Enables the platform to offer unique challenges to each trainee, preventing the sharing of solutions and encouraging independent problem-solving.
*   **Realistic Scenarios**: Allows for the dynamic generation of realistic credentials, network configurations, or flag values, making exercises more authentic and less predictable.
*   **Automated Content Creation**: Reduces the manual effort required to create diverse training content, allowing instructors to focus on designing scenarios rather than generating individual data points.
*   **Deterministic Randomness**: While random, the generation process can be seeded (as suggested by its usage in `backend-ansible-runner`), ensuring that specific sandboxes or challenges can be re-created consistently for analysis or debugging.

This library is a powerful tool that significantly enhances the adaptive and dynamic capabilities of the CyberRangeCZ platform, making training more effective and impactful.
