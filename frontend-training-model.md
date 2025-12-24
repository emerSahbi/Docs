# frontend-training-model

This repository contains an Angular library that defines the data model for all training-related features in the CyberRangeCZ platform. It serves as the single source of truth for the data structures used across the training frontend. Although the code has been merged into the `frontend-platform` monorepo, this documentation describes the original structure and purpose of the repository.

## Key Functionality:

The `frontend-training-model` library provides a comprehensive set of TypeScript classes, interfaces, and enums that represent the data structures for the training lifecycle. It does not contain any components or services, but it is a critical dependency for other frontend libraries that do.

The data model is organized into the following categories:

*   **Core Training Entities**: The fundamental building blocks of the training module.
    *   `TrainingDefinition`: Represents the template for a training exercise.
    *   `TrainingInstance`: Represents a specific instance of a training definition.
    *   `TrainingRun`: Represents a user's attempt at a training instance.

*   **Content Structure**: The models for structuring the training content.
    *   `Level`: A training is divided into levels, which can be of different types (e.g., `AssessmentLevel`, `InfoLevel`).
    *   `Phase`: Each level is composed of phases, which are the smallest units of the training content (e.g., `TrainingPhase`, `QuestionnairePhase`).

*   **Assessments**: A rich data model for creating assessments within the training.
    *   `Question`: A variety of question types are supported, including `MultipleChoiceQuestion`, `FreeFormQuestion`, and `ExtendedMatchingItems`.

*   **User Roles**: The different roles that a user can have in the training context.
    *   `Trainee`: A user who is taking the training.
    *   `Organizer`: A user who is managing the training.
    *   `Designer`: A user who is creating the training content.

*   **Cheating Detection**: A detailed data model for identifying and flagging potential cheating.
    *   `DetectionEvent`: Represents a specific cheating event, with different types for different cheating methods (e.g., `AnswerSimilarityDetectionEvent`, `ForbiddenCommandsDetectionEvent`).

*   **MITRE Techniques**: A model for integrating the MITRE ATT&CK framework into the training content.

*   **Enumerations**: A large set of enums that define the possible states and types for the various entities (e.g., `TrainingRunState`, `QuestionType`).

## Role in CyberRangeCZ:

The `frontend-training-model` library is a cornerstone of the frontend architecture. It ensures that all other frontend libraries are using the same data structures, which provides:

*   **Consistency**: It eliminates data-related conflicts and inconsistencies between different parts of the application.
*   **Type Safety**: By using TypeScript, it provides strong type checking at compile time, which reduces the number of bugs.
*   **Maintainability**: By centralizing the data model, it makes the code easier to understand, maintain, and evolve.

In essence, this library provides the vocabulary that the rest of the training frontend uses to communicate and operate.
