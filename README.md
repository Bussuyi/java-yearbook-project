# DevOps Modern End-to-End Deployment

![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![Java](https://img.shields.io/badge/Java-21-orange)
![Maven](https://img.shields.io/badge/Maven-Build-red)
![Terraform](https://img.shields.io/badge/Terraform-IaC-purple)
![Ansible](https://img.shields.io/badge/Ansible-Automation-black)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-red)

## Project Overview

This project implements an automated DevOps pipeline
to provision AWS infrastructure and deploy two
applications on a single EC2 instance.

The deployment uses Infrastructure as Code,
configuration management, containerization,
and CI/CD automation.

## Applications

1. Personal Portfolio Website
2. Java Yearbook Application

## Technologies Used

- AWS
- Terraform
- Ansible
- Docker
- Docker Compose
- Git and GitHub
- GitHub Actions
- Java
- Maven
- Ubuntu Linux

## Project Architecture

GitHub
   |
   v
GitHub Actions
   |
   v
Maven Build
   |
   v
Terraform
   |
   v
AWS EC2
   |
   v
Ansible
   |
   v
Docker Compose
   |
   +----------------+
   |                |
   v                v
Portfolio App     Java App
Port 80           Port 8081

## Infrastructure

Terraform provisions:

- Custom AWS VPC
- Internet Gateway
- Public Subnet
- Route Table
- Security Group
- EC2 Instance

## Configuration Management

Ansible performs:

- Ubuntu package updates
- Docker installation
- Docker Compose installation
- Application file transfer
- Application deployment

## Containerization

Docker packages both applications.

Docker Compose manages both containers
on the same EC2 server.

## CI/CD Pipeline

GitHub Actions automates:

1. Repository checkout
2. Java application build
3. Terraform initialization
4. AWS infrastructure provisioning
5. EC2 public IP retrieval
6. Ansible inventory generation
7. Server configuration
8. Docker application deployment

## Application URLs

Portfolio:
http://35.170.67.19

Java Application:
http://35.170.67.19:8081

## Deployment Instructions

1. Clone the GitHub repository.
2. Install the required development tools.
3. Configure AWS access.
4. Configure Terraform.
5. Provision the AWS infrastructure.
6. Configure the EC2 server with Ansible.
7. Build and deploy the Docker containers.
8. Configure GitHub Actions for automated deployment.

## Security

- AWS credentials are not committed to GitHub.
- SSH private keys are stored securely.
- GitHub Actions authenticates through AWS OIDC.
- Terraform state is stored in an encrypted S3 bucket.

## Conclusion

This project demonstrates an end-to-end automated
DevOps deployment using AWS, Terraform, Ansible,
Docker, Docker Compose and GitHub Actions.
