# Build and Deploy Using Script

This guide provides step-by-step instructions to build the Smart NVR Sample Application using script. You'll learn how to:
- Build the required images for the application.
- Start the application and ensure all services are running.
- Verify the deployment to confirm the application is functioning correctly.

## Setup the environment variables
- Setup the following environment variables
  ```bash
     export FRIGATE_IP=<frigate-ip-address> #IP address of the Frigate VMS (required)
     export FRIGATE_PORT=<frigate-port> #Port of the Frigate VMS (required, typically 5000)
     export VSS_SUMMARY_IP=<vss-ip-address> #IP address of the Video Summarization service (required)
     export VSS_SUMMARY_PORT=<vss-port> #Port of the Video Summarization service (required, typically 12345)
     export VSS_SEARCH_IP=<vss-ip-address> #IP address of the Video Search service (required)
     export VSS_SEARCH_PORT=<vss-port> #Port of the Video Search service (required, typically 12345)
     export VLM_MODEL_IP=<vlm-model-end-point-ip-address> #IP address of the VLM Model Endpoint (required)
     export VLM_MODEL_PORT=<vlm-model-end-point-port> #Port of the VLM Model Endpoint (required, typically 9766)
     export MQTT_USER=<mqtt-user> #Add your mqtt user          
     export MQTT_PASSWORD=<pwd> #Add your mqtt password
     export HOST_IP=<host-ip>  # It's the IP address where the NVR Event Router will run
  ```

## Build the images
Clone the repository if not already done.
```bash
git clone https://github.com/open-edge-platform/edge-ai-suites.git
cd edge-ai-suites/metro-ai-suite/smart-nvr
```
A script is provided to ease the task of building the images as well manage the built images. Run the following command to build the images. This will initiate building process of the required images:
  ```bash
  ./build.sh
  ```

## What to Do Next
- **[Get Started](./get-started.md)**: Ensure you have completed the initial setup steps before proceeding.
- **[Troubleshooting Docker Deployments](./support.md#troubleshooting-docker-deployments)**: Find detailed steps to resolve common issues during Docker deployments.

