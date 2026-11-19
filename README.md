CloudSync – CI/CD Automation with Jenkins, Docker & AWS EKS

1. Project Overview
CloudSync is a DevOps project that automates the build and deployment of a web application on Amazon EKS
using Jenkins, Docker,and Kubernetes.
The project implements a CI/CD pipeline that builds Docker images, pushes them to Docker Hub,
and deploys the application to an AWS EKS cluster.

3. Project Architecture
Workflow
1. Developer pushes code to GitHub.
2. Jenkins triggers the CI/CD pipeline.
3. Jenkins builds the Docker image.
4. Docker image is pushed to Docker Hub.
5. Jenkins connects to the AWS EKS cluster.
6. Kubernetes deploys the updated application.
7. AWS LoadBalancer exposes the application to end users.

