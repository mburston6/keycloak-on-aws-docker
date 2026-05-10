Keycloak on AWS Docker
Overview

This project demonstrates the deployment of the Keycloak Identity and Access Management (IAM) platform on AWS EC2 using Docker containers.

The deployment included:

AWS EC2 Linux server configuration
AWS security group configuration
Docker installation and container management
Keycloak deployment and configuration
Realm and user creation
Authentication testing and troubleshooting
Technologies Used
AWS EC2
Amazon Linux 2023
Docker
Keycloak
Linux CLI
SSH
IAM / Authentication Concepts
Architecture

Browser
↓
AWS Security Group
↓
EC2 Linux Server
↓
Docker Container
↓
Keycloak IAM Platform

Deployment Process
1. Created AWS Security Group

Configured inbound rules for:

SSH (Port 22)
Keycloak Web Access (Port 8080)
2. Launched EC2 Instance
Amazon Linux 2023
t2.micro instance
Public IP enabled
3. Connected via SSH

Used SSH private key authentication from Windows PowerShell.

4. Installed Docker

Installed and configured Docker runtime environment on the EC2 instance.

5. Deployed Keycloak Container

Deployed Keycloak using Docker with HTTP enabled for lab purposes.

6. Configured Keycloak
Created lab realm
Created test user
Configured credentials
Verified successful authentication
Troubleshooting

During deployment, Keycloak enforced HTTPS requirements by default. The issue was resolved by changing the realm SSL requirement setting to:

Require SSL = None

This allowed HTTP authentication for the lab environment.

Skills Demonstrated
Cloud Infrastructure Deployment
Linux Administration
Docker Containerization
Identity and Access Management (IAM)
Networking and Security Configuration
Authentication Testing
Troubleshooting and Debugging
Screenshots

Deployment screenshots are included in this repository.
