# DevOps Bootcamp Capstone Project

Welcome to the DevOps Bootcamp Capstone Project repository! This project demonstrates the setup and deployment of a web application using various technologies, including Terraform, Docker, and GitHub Actions. The objective is to run the application on Amazon EKS (Elastic Kubernetes Service) and access it through the Load Balancer DNS URL.

## Getting Started

Before getting started, it's recommended to run through the manual steps to ensure a smooth deployment process.

### Step 1: Manual Setup

1. Install terraform [Click here to visit Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
2. Install awscli [Click here to visit AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

### Step 2: Run Terraform Scripts

To deploy the infrastructure, follow these steps:

1. Navigate to the `terraform` directory.
2. Run the following commands:

   ```shell
   terraform init
   terraform plan
   terraform apply --auto-approve
![Terraform Commands](screenshots/vpc.PNG)
![Terraform Commands](screenshots/BASTION_HOST.PNG)
![Terraform Commands](screenshots/cluster.PNG)
![Terraform Commands](screenshots/ECR.PNG)
![Terraform Commands](screenshots/EIP.PNG)
![Terraform Commands](screenshots/internet_gateway.PNG)
![Terraform Commands](screenshots/LOADBALANCERS.PNG)
![Terraform Commands](screenshots/NAT.PNG)
![Terraform Commands](screenshots/node_group.PNG)
![Terraform Commands](screenshots/security_groups.PNG)
![Terraform Commands](screenshots/subnet.PNG)

## Amazon EKS Cluster Setup and Docker Image Deployment

This section guides you through updating your kubeconfig for an Amazon EKS cluster and pushing Docker images to an ECR repository.

### Step 3: Update Kubeconfig for Amazon EKS Cluster

To update the kubeconfig for your Amazon EKS cluster, execute the following command:

```shell
aws eks update-kubeconfig --name hr-stag-eksdemo1 --region us-east-1
