# Get Help

This page provides comprehensive support and troubleshooting information for the Smart NVR Sample Application. It is divided into the following sections:

  - **Common Issues**: General troubleshooting steps for resolving issues like container failures, port conflicts, and missing dependencies.
  - **Troubleshooting Docker Deployments**: Steps to address problems specific to Docker deployments.
  - **Troubleshooting Helm Deployments**: Guidance for resolving issues in Helm-based deployments.

## Troubleshooting Common Issues

### 1. Containers Not Starting
- **Issue**: The application containers fail to start.
- **Solution**:

  ```bash
  docker compose logs
  ```
  Check the logs for errors and resolve dependency issues.

### 2. Port Conflicts
- **Issue**: Port conflicts with other running applications.
- **Solution**: Update the ports section in the Docker Compose file.

### 3. Missing Dependencies
- **Issue**: Required software dependencies are not installed.
- **Solution**:

  ```bash
  sudo apt-get install -y <dependency>
  ```

## Troubleshooting Docker Deployments

### 1. Containers Failing To Start:
   - Check the Docker logs for errors:
     ```bash
     docker compose logs
     ```
### 2. Port Conflicts:
   - Update the `ports` section in the Compose file to resolve conflicts.
### 3. Reset Application:
   - Follow these steps to reset the application to the initial state
     ```bash
     docker compose down
     docker volume ls | grep vms-event-router | awk '{ print $2 }' | xargs docker volume rm
     ```
<!--
## Support
- **Developer Forum**: Join the community forum
- **Contact Support**: [Support Page](#)
-->
