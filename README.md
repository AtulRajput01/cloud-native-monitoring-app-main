# Cloud Native Resource Monitoring Python App

### Introduction

This project aims to provide hands-on learning experience in developing and deploying a cloud-native resource monitoring Python application on Kubernetes (K8s). The aim of this assignment is to understand the hands-on experience with GitOps practices, utilizing Argo CD for continuous deployment and Argo Rollouts for advanced deployment strategies within a Kubernetes environment. You will be responsible for setting up a GitOps pipeline that automates the deployment and management of a simple web application. Key objectives include understanding Python for developing monitoring applications, Docker for containerization, AWS for hosting the application, and Kubernetes for orchestration.


## Prerequisites

Before starting the project, ensure you have the following prerequisites:

- Familiarity with Kubernetes concepts (Pods, Deployments, Services).
- Basic understanding of Docker and containerization.
- Experience with Git for version control.
- Access to a Kubernetes cluster for testing (you can use Minikube, kind, or a cloud provider's Kubernetes service).
- Familiarity with Argo CD and Argo Rollouts tools. Refer to the documentation for the basics of these tools.

Additionally, make sure you have the following installed:

- AWS Account with programmatic access configured via AWS CLI.
- Python3 installed on your local machine.
- Docker and Kubectl installed.
- A code editor such as Visual Studio Code.


## Getting Started

### Part 1: Deploying the Flask Application Locally

#### Step 1: Clone the Repository

Clone the repository using the following command:

 git clone https://github.com/AtulRajput01/cloud-native-resource-monitoring-app.git


2. **Install Dependencies**
- Install dependencies using pip:
  ```
  pip3 install -r requirements.txt
  ```

3. **Run the Application Locally**
- Navigate to the root directory of the project and execute:
  ```
  $ python3 app.py
  ```

# Overview of Using Argo CD for Continuous Deployment

## Setup and Configuration

1. **Installation:** Argo CD is installed on the Kubernetes cluster following the official documentation.
2. **Configuration:** Once installed, it's configured to monitor a specific Git repository containing Kubernetes manifests for the application.

## Creating the GitOps Pipeline

1. **Dockerization:** After dockerizing the application and pushing the Docker image to a container registry, Argo CD is set up to monitor changes in the repository.
2. **Continuous Deployment:** Argo CD automatically deploys any changes pushed to the repository to the Kubernetes cluster, ensuring continuous deployment.

## Implementing a Canary Release with Argo Rollouts

1. **Extension Usage:** Argo Rollouts, an extension of Argo CD, is utilized to implement a canary release strategy.
2. **Rollout Definition:** The rollout definition is modified to specify the canary release strategy, allowing for controlled testing of new versions of the application before full deployment.


![alt text](<Screenshot from 2024-05-16 16-59-45.png>)
3. **Monitoring:** Changes to the application code trigger a rollout, with Argo Rollouts monitoring the deployment process to ensure the canary release completes successfully.

![alt text](<Screenshot from 2024-05-16 16-06-56.png>)


Argo CD simplifies the deployment process by providing a centralized platform for managing application deployments in Kubernetes clusters. It promotes GitOps practices, enhancing collaboration and automation in the software development lifecycle.

## Documentation

[Link to Detailed Documentation](https://docs.google.com/document/d/1GRSvt9kFFUHPZhuZW7NYbihq1ClK47WMCGZVaMo9DRc/edit?usp=sharing)