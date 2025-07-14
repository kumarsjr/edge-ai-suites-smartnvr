# Build and Deploy Using Docker Compose

This guide provides step-by-step instructions to build and deploy the Smart NVR Sample Application using Docker Compose. You'll learn how to:
- Build the required images for the application.
- Start the application and ensure all services are running.
- Verify the deployment to confirm the application is functioning correctly.

Docker Compose simplifies the deployment process by managing multiple containers as a single application. For more details, see [Docker Compose Documentation](https://docs.docker.com/compose/).

## Setup the environment variables
- Setup the following environment variables
  ```bash
  export FRIGATE_IP=<frigate-ip-address> #IP address of the Frigate VMS (required)
  export FRIGATE_PORT=<frigate-port> #Port of the Frigate VMS (required, typically 5000)
  export VSS_IP=<vss-ip-address> #IP address of the Video Search and Summarization service (required)
  export VSS_PORT=<vss-port> #Port of the Video Search and Summarization service (required, typically 12345)
  export VLM_MODEL_IP=<vlm-model-end-point-ip-address> #IP address of the VLM Model Endpoint (required)
  export VLM_MODEL_PORT=<vlm-model-end-point-port> #Port of the VLM Model Endpoint (required, typically 9766)
  ```

## Build the images
Clone the repository if not already done.
```bash
git clone https://github.com/open-edge-platform/edge-ai-suites.git
cd edge-ai-suites/metro-ai-suite/smart-nvr
```
A script is provided to ease the task of building the images as well manage the built images. Run the following command to build the image.
  ```bash
  source ./build.sh
  ```

## Run the application
The script provides an option to start all the required services.
  ```bash
  ./setup.sh start
  ```
The following services will be built as shown in the below screenshot.
![Services overview](./_images/containers.png)

To stop the application at any point of time, the same script can be used as follows.
  ```bash
  ./setup.sh stop
  ```

Verify the Application: Check that the application is running:
```bash
docker compose ps
```

## What to Do Next
- **[Troubleshooting Docker Deployments](./support.md#troubleshooting-docker-deployments)**: Find detailed steps to resolve common issues during Docker deployments.
- **[Get Started](./get-started.md)**: Ensure you have completed the initial setup steps before proceeding.
