# terraform-web
Simple Website Deployment with Terraform and AWS

Project Overview

This project demonstrates how to use Terraform to provision an AWS EC2 instance, install a web server, and serve a basic webpage. The entire infrastructure is managed as code and can be easily deployed or destroyed.

Prerequisites

Ensure you have the following installed and configured:

Terraform

AWS CLI

An AWS account with IAM permissions to create EC2 instances and security groups

Git

Infrastructure Components

This Terraform script provisions:

VPC: A virtual private cloud for networking.

Subnet: A public subnet for the EC2 instance.

Security Group: Allows inbound HTTP (80) and SSH (22) traffic.

EC2 Instance: Hosts an Apache web server with a simple HTML page.

Deployment Steps

1. Clone the Repository

git clone <your-github-repo-url>
cd terraform-web

2. Initialize Terraform

terraform init

3. Apply the Terraform Configuration

terraform apply -auto-approve

Terraform will output the public IP of the EC2 instance. Open a browser and enter:

http://<PUBLIC_IP>

You should see a simple webpage saying "Hello from Terraform".

4. Destroy the Infrastructure (When Done)

terraform destroy -auto-approve

File Structure

terraform-web/
│── main.tf       # Terraform configuration file
│── README.md     # Documentation (this file)
│── .gitignore    # Files to ignore in Git

Future Enhancements

Host a static website on AWS S3 instead of EC2

Automate deployments using GitHub Actions

Use Terraform modules for better structure