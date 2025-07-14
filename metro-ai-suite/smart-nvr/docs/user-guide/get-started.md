# Get Started

<!--
**Sample Description**: Provide a brief overview of the application and its purpose.
-->
The Smart NVR sample application brings GenAI-powered vision analytics to traditional network video recorders, enabling intelligent event detection and real-time insights directly at the edge. With this guide, you’ll quickly deploy, configure, and experience advanced video analytics capabilities that help you manage and extract value from your video data.

## Prerequisites
- Verify that your system meets the [Minimum Requirements](./system-requirements.md).
- Install Docker: [Installation Guide](https://docs.docker.com/get-docker/).
- Enable running docker without "sudo": [Post Install](https://docs.docker.com/engine/install/linux-postinstall/)
- Install Git: [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- VLM microservice running a device to connect to NVR.
- VSS running in two devices in search and summary mode.
- Containers built using [How to build from source](./how-to-build-from-source.md)

<!--
**Setup and First Use**: Include installation instructions, basic operation, and initial validation.
-->
## Set up and First Use

<!--
**User Story 1**: Setting Up the Application  
- **As a developer**, I want to set up the application in my environment, so that I can start exploring its functionality.

**Acceptance Criteria**:
1. Step-by-step instructions for downloading and installing the application.
2. Verification steps to ensure successful setup.
3. Troubleshooting tips for common installation issues.
-->

1. **Clone the Repository**:
   - Run the following command to create a local repo.
     ```bash
     git clone https://github.com/open-edge-platform/edge-ai-suites.git
     cd edge-ai-suites/metro-ai-suite/smart-nvr
     ```

2. **Setup required environment variables**:
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
   
3. # Run the application
The script provides an option to start all the required services.
  ```bash
  ./setup.sh start
  ```
The following services will be built as shown in the below screenshot.
![Services overview](./_images/containers.png)



4. **Access the Application**:
   Open a browser and go to `http://<host-ip>:7860` to access the application.

5. To stop the application at any point of time, the same script can be used as follows.
  ```bash
  ./setup.sh stop
  ```

## Supporting Resources
> **Note**: Users are advised to use the build process mentioned below for this release which uses a build script which directly builds the images.
- [How to build from source](./how-to-build-from-source.md): How to build and deploy the application using Docker Compose.
