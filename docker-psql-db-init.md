# docker-psql-db-init

This repository defines a specialized Docker image (`docker-psql-db-init`) that serves as a **utility for initializing PostgreSQL database instances**. It extends the official `postgres:14` Docker image with a custom entrypoint script that automates the creation of a new database user and a new database, assigning ownership of the database to the newly created user.

## Key Functionality:

*   **Automated Database Setup**: Streamlines the process of setting up a PostgreSQL database and user accounts, which is a common prerequisite for many microservices.
*   **Dynamic Configuration**: Relies on environment variables to receive all necessary parameters for database connection and user/database creation:
    *   `HOST`: The hostname or IP address of the PostgreSQL server.
    *   `PORT`: The port number of the PostgreSQL server.
    *   `ADMIN_USER`: A PostgreSQL user with administrative privileges (e.g., `postgres`).
    *   `ADMIN_PASSWORD`: The password for the admin user.
    *   `USER`: The desired username for the new database user.
    *   `PASSWORD`: The password for the new database user.
    *   `DBNAME`: The name of the database to be created.
*   **Database Availability Check**: The entrypoint script includes a wait mechanism (`pg_isready`) to ensure the target PostgreSQL database is fully operational before attempting any initialization steps, enhancing reliability.
*   **Idempotent Operations**: The script checks for the existence of the user and database before attempting to create them, ensuring that repeated executions do not cause errors.
*   **User and Ownership Management**: Creates a new PostgreSQL role (user) with the specified credentials and then grants ownership of the newly created (or existing) database to this user.

## Role in CyberRangeCZ:

This `docker-psql-db-init` image is a vital operational tool within the CyberRangeCZ platform's microservices architecture:

*   **Microservice Database Provisioning**: Many backend services within CyberRangeCZ require their own dedicated PostgreSQL databases. This image automates the setup of these databases during deployment, simplifying the overall orchestration.
*   **Consistent Database Environments**: Ensures that each service's database is initialized in a consistent and standardized manner, reducing configuration drift and potential issues.
*   **Simplified Deployment Workflows**: By encapsulating database initialization logic, it makes the deployment process for database-backed services more robust and less prone to manual errors.
*   **Security Best Practices**: Encourages the use of dedicated database users with appropriate ownership, aligning with the principle of least privilege.

By automating the initial setup of PostgreSQL databases, this utility image significantly contributes to the efficiency and reliability of deploying the data layer for CyberRangeCZ's various backend services.
