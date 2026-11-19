CloudSync – CI/CD Automation with Jenkins, Docker & AWS EKS

1. Project Overview :
   
CloudSync is a DevOps project that automates the build and deployment of a web application on Amazon EKS using Jenkins, Docker, and Kubernetes.
The project implements a CI/CD pipeline that builds Docker images, pushes them to Docker Hub, and deploys the application to an AWS EKS cluster.

2. Project Architecture:
 
Workflow
- Developer pushes code to GitHub.
- Jenkins triggers the CI/CD pipeline.
- Jenkins builds the Docker image.
- Docker image is pushed to Docker Hub.
- Jenkins connects to the AWS EKS cluster.
- kubernetes deploys the updated application.
- AWS LoadBalancer exposes the application to end users.

   <img width="1262" height="732" alt="CloudSync - Architecture" src="https://github.com/user-attachments/assets/df2b0d10-0be9-4fae-8c0d-f5a68c709dfb" />


3. Technologies Used:
 
Category	            Tools

Cloud	               AWS (EC2, EKS, IAM)
CI/CD	               Jenkins
Version Control	   Git, GitHub
Containerization	   Docker
Container Registry	Docker Hub
Orchestration	      Kubernetes
Web Server	         Apache

4. Project Structure:
``` 
CloudSync-project/
│
├── Jenkinsfile
├── index.html
├── Dockerfile
├── images/
│   ├── tooplate-cloud-sync-bg01.jpg
│   ├── tooplate-cloud-sync-bg02.jpg
│   └── tooplate-cloud-sync-bg03.jpg
│
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
│
├── screenshots/
│   ├── architecture.png
│   ├── jenkins-pipeline.png
│   ├── eks-deployment.png
│   └── application-running.png
│
└── README.md
```

5. Jenkins CI/CD Pipeline:
 The Jenkins pipeline automates the following stages:
- Builds the Docker image using the Dockerfile.
- Tags the image using the Jenkins build number.
- Pushes the image to Docker Hub.
- Configures AWS EKS access.
- Deploys Kubernetes manifests.
- Updates the Kubernetes deployment with the latest image.
- Verifies the deployment rollout.
Jenkins Pipeline Execution

<img width="1866" height="915" alt="CloudSync - Jenkins pipeline screenshot" src="https://github.com/user-attachments/assets/d73b71dc-1ee0-4f7b-b28b-30d9f5325887" />




6. AWS EKS Deployment:
The application is deployed on Amazon EKS using Kubernetes.
- Deployment: Manages application Pods.
- Pods: Run the Dockerized application.
- Service: Exposes the application using AWS LoadBalancer.


<img width="1126" height="973" alt="CloudSync - EKS Deployment" src="https://github.com/user-attachments/assets/bc40a7fd-5055-4945-9321-084efa45d7f4" />




<img width="1920" height="950" alt="CloudSync - Application running screenshot" src="https://github.com/user-attachments/assets/71299b1d-5c3d-4c78-8c5f-1c8d7158dcd5" />




7. Prerequisites:
- AWS account and configured EKS cluster.
- Jenkins server.
- Docker and Docker Hub account.
- Git and GitHub.
- AWS CLI and kubectl.
- Required AWS and Docker Hub credentials configured in Jenkins.

8. Key Features:
- Automated CI/CD using Jenkins.
- GitHub integration.
- Automated Docker image build and push.
- Kubernetes-based application deployment.
- Version-based Docker image tagging.
- Application access through AWS LoadBalancer.
- Automated deployment verification.

9. Future Enhancements:
- Terraform for infrastructure provisioning.
- Prometheus and Grafana for monitoring.
- SonarQube for code quality.
- Trivy for container image scanning.
- Kubernetes Horizontal Pod Autoscaler.

10. Learning Outcomes:
- Hands-on experience with Jenkins CI/CD pipelines.
- Docker image creation and management.
- AWS EKS cluster management.
- Kubernetes deployments, Pods, and Services.
- CI/CD automation and deployment troubleshooting.
