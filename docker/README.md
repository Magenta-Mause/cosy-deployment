# Docker Compose Setup for Cosy Application

This directory contains the Docker Compose setup to run the Cosy application locally.

## Project Structure

*   **`docker-compose.yml`**: Defines the services (backend, frontend, database), networks, and volumes for the application.
*   **`.env`**: Stores environment variables, particularly for database credentials. **Remember to keep this file secure and do not commit sensitive information.**
*   **`backend.Dockerfile`**: A placeholder Dockerfile for the backend service. If you wish to build the backend from source, replace this file with your actual `Dockerfile`.
*   **`frontend.Dockerfile`**: A placeholder Dockerfile for the frontend service. If you wish to build the frontend from source, replace this file with your actual `Dockerfile`.

## Running the Application

1.  **Navigate to this directory:**
    ```bash
    cd cosy-deployment/docker
    ```

2.  **Start the services:**
    ```bash
    docker-compose up
    ```
    This command will pull the specified pre-built Docker images (as defined in `docker-compose.yml`) and start the services.

3.  **To run services in detached mode (in the background):**
    ```bash
    docker-compose up -d
    ```

4.  **To stop and remove containers, networks, and volumes:**
    ```bash
    docker-compose down
    ```

## Building from Source (if applicable)

If you have the source code for the backend and frontend and wish to build your own Docker images:

1.  **Replace Placeholder Dockerfiles:** Update `backend.Dockerfile` and `frontend.Dockerfile` with the actual build instructions for your respective applications.
2.  **Build the images:**
    ```bash
    docker-compose build
    ```
3.  **Start the services:**
    ```bash
    docker-compose up
    ```

## Configuration

The `.env` file contains critical environment variables. Ensure these are correctly set before running the application.

*   `POSTGRES_USER`: Username for the PostgreSQL database.
*   `POSTGRES_PASSWORD`: Password for the PostgreSQL database.

