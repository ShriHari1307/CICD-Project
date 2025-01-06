# Complete CI/CD Pipeline using Jenkins

## About the Project

This project demonstrates the creation of a complete CI/CD pipeline using **Jenkins**, integrated with tools like **SonarQube** for code quality analysis, **Nexus OSS** for artifact management, and **AWS EKS** for scalable deployment of containerized applications. The pipeline automates the entire build, test, and deployment process, ensuring faster and more reliable delivery of applications.

## Key Features
- **Jenkins**: Orchestrates the CI/CD pipeline.
- **SonarQube**: Performs code quality analysis.
- **Nexus OSS**: Manages and stores build artifacts.
- **Docker**: Containerizes the application.
- **AWS EKS**: Deploys the containerized application in a scalable Kubernetes environment.
- **Maven**: Handles project dependencies and builds.
- **Git Bash**: Version control and repository management.
- **AWS EC2**: Hosts Jenkins, SonarQube, and Nexus OSS on separate virtual machines.

---

## Steps to Set Up the Pipeline

### 1. **Set Up AWS EC2 Instances**
   - Create three separate EC2 instances:
     - **Jenkins Instance**: For running Jenkins.
     - **SonarQube Instance**: For code quality analysis.
     - **Nexus OSS Instance**: For artifact repository.

### 2. **Install Required Tools**
   - On each instance, install the necessary dependencies:
     - **Jenkins Instance**:
       - Install Jenkins and required plugins.
       - Configure Git and Maven.
     - **SonarQube Instance**:
       - Install and configure SonarQube.
       - Ensure SonarQube is accessible via its web interface.
     - **Nexus OSS Instance**:
       - Install Nexus OSS and configure repository management.

### 3. **Connect Jenkins to Other Tools**
   - Configure **SonarQube** and **Nexus OSS** in Jenkins.
   - Add the respective credentials and server URLs in Jenkins.

### 4. **Set Up the CI/CD Pipeline**
   - Create a `Jenkinsfile` to define the pipeline stages:
     1. **Clone Code**: Pull source code from the Git repository.
     2. **Build**: Use Maven to build the project and generate artifacts.
     3. **Code Quality**: Analyze the code using SonarQube.
     4. **Artifact Management**: Push the generated artifacts to Nexus OSS.
     5. **Dockerize**: Build Docker images for the application.
     6. **Deploy**: Deploy the application to AWS EKS.

### 5. **Configure AWS EKS**
   - Set up an EKS cluster on AWS.
   - Deploy Kubernetes manifests (e.g., Deployment, Service) for the application.

### 6. **Run the Pipeline**
   - Trigger the pipeline from Jenkins.
   - Monitor the stages, ensuring successful execution at each step.

---

## Additional Notes
- **Prerequisites**:
  - Basic knowledge of Jenkins, Docker, and Kubernetes.
  - An AWS account with sufficient permissions.
  - Access to a Git repository with the application source code.
- Ensure security best practices by managing credentials securely in Jenkins.
- Monitor resource usage on EC2 instances to optimize performance.

---

This project showcases a robust and scalable CI/CD pipeline that can be adapted for various applications and environments.
