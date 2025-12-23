# backend-training-feedback

This repository contains the "CyberRangeCZ Platform Training Feedback" backend microservice. Its primary purpose is to **process data related to cybersecurity training exercises to generate automated feedback for participants and provide structured data for various visualizations** within the CyberRangeCZ platform. This service plays a crucial role in the pedagogical aspect of the platform, transforming raw trainee activity into actionable insights and graphical representations of progress and performance.

## Key Technologies and Features:

*   **Java with Spring Boot**: Developed using Java and the Spring Boot framework (version 2.6.2, Java 17), providing a robust and scalable foundation for a microservice.
*   **RESTful API**: Exposes a well-defined RESTful API at `/training-feedback/api/v1` for collecting and providing feedback-related data. API documentation is generated using Swagger/Springfox, with its host configured for `localhost:8087` in `pom.xml` (though the `README.md`'s Docker run example uses `8083`).
*   **Data Persistence**: Utilizes Spring Data JPA for data management, supporting both in-memory H2 database (for development/testing) and PostgreSQL (for production environments). Flyway is used for managing database schema migrations.
*   **Advanced Data Querying**: Integrates **QueryDSL** for building type-safe and sophisticated database queries, essential for extracting meaningful patterns and metrics from training data to generate feedback.
*   **Reactive Web Capabilities**: Includes `spring-boot-starter-webflux`, suggesting it can handle reactive, non-blocking requests, which is beneficial for processing potentially large volumes of training data or feedback submissions efficiently.
*   **Utility Libraries**: Leverages `Javatuples` for working with tuple-like data structures and `Apache Commons Text` for advanced text manipulation, possibly for processing log entries or generating summarized feedback.
*   **Code Quality and Security**: Adheres to the platform's rigorous standards for code quality and security, integrating tools like Spotless, Surefire, Checkstyle, SpotBugs, and OWASP Dependency-Check during the build process.
*   **Containerization**: Designed for deployment as a Docker container, making it easily manageable and scalable within the platform's microservices architecture.

## Role in CyberRangeCZ:

The `backend-training-feedback` service is indispensable for enhancing the learning experience and evaluation capabilities of the CyberRangeCZ platform:

*   **Automated Feedback Generation**: Processes trainee performance data and actions to generate objective and timely feedback, helping participants understand their strengths and weaknesses.
*   **Data for Visualizations**: Provides the structured data necessary for frontend components to render various graphs and charts (e.g., progress over time, performance against objectives, common errors), giving a visual overview of training outcomes.
*   **Training Content Improvement**: By analyzing aggregated feedback, instructors can identify areas where training materials or scenarios need improvement.
*   **Performance Analytics**: Offers insights into individual and group performance, which can be used for reporting and further educational research.

This service transforms raw training interactions into valuable educational insights, significantly contributing to the effectiveness and analytical power of the CyberRangeCZ training platform.
