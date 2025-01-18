CICD Manifest Repository

This repository contains Kubernetes manifests used for deploying and managing applications as part of a Continuous Integration and Continuous Deployment (CI/CD) pipeline. It includes YAML configurations for deploying pods, services, and other resources.


Directory Structure


/Deploy/

│

├── deploy.yaml    # Contains configurations for deployment

├── pod.yaml       # Defines the Kubernetes pod specifications

├── service.yaml   # Configures the Kubernetes service for exposing the application


Purpose

The cicd-manifest-repo is designed to be used in CI/CD pipelines to automate the deployment process for applications running on Kubernetes. In this process, Jenkins and ArgoCD play key roles:

•	Jenkins: Acts as the Continuous Integration (CI) tool responsible for building, testing, and packaging the application. It trigger deployments by updating configuration files in this repository (the source of truth) and pushing changes to the appropriate branch.

•	ArgoCD: Serves as the Continuous Deployment (CD) tool that monitors this repository (the source of truth) for changes and automatically synchronizes the Kubernetes cluster with the updated manifest files. 

By adopting a GitOps approach, ArgoCD ensures the desired state defined in the repository matches the actual state in the cluster, providing consistency and traceability.


File Descriptions

•	deploy.yaml
:-  Configuration file for the deployment, including replicas, container images, and other deployment-specific configurations.

•	pod.yaml
:-  Describes the specifications for the Kubernetes pod, including container configurations and resource requirements.

•	service.yaml
:-  Defines the Kubernetes service to expose the application to internal or external networks.
