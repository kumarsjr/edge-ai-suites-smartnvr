# Build and Deploy Using Docker Compose

This guide provides step-by-step instructions to build and deploy the Smart NVR Sample Application using Docker Compose. You'll learn how to:
- Build the required images for the application.
- Start the application and ensure all services are running.
- Verify the deployment to confirm the application is functioning correctly.

Docker Compose simplifies the deployment process by managing multiple containers as a single application. For more details, see [Docker Compose Documentation](https://docs.docker.com/compose/).

## Setup the environment variables


## Build the images


## Run the application

- Use Docker Compose to start the application:
  ```bash
  docker compose up -d
  ```

- Verify the Application: Check that the application is running:
  ```bash
  docker compose ps
  ```

## What to Do Next
- **[Troubleshooting Docker Deployments](./support.md#troubleshooting-docker-deployments)**: Find detailed steps to resolve common issues during Docker deployments.
- **[Get Started](./get-started.md)**: Ensure you have completed the initial setup steps before proceeding.
