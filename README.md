# Dockerized Web Application Deployment on AWS

This project orchestrates the deployment of a dynamic web application on Amazon Web Services (AWS) leveraging Docker. It encompasses configuring local environment variables, building AWS infrastructure, creating Docker images, pushing these images to AWS, importing data, configuring ECS service, establishing an Application Load Balancer (ALB), provisioning an SSL certificate, and configuring Route 53 for DNS resolution.
## Prerequisites
1. AWS account
2. Docker installed locally

## Setting Up Local Environment
1. Clone the repository containing the web application code.
2. Set up local environment variables as per the application requirements.

## Building AWS Infrastructure
1. Create a 3-tier VPC (Virtual Private Cloud).
2. Set up a NAT Gateway (NGW).
3. Configure security groups for necessary inbound and outbound traffic.
4. Provision an RDS (Relational Database Service) instance.

## Building Docker Image
1. Write a Dockerfile for the web application.
2. Set build arguments for environment variables in the Dockerfile.
3. Build the Docker image locally.

## Pushing Docker Image to AWS
1. Tag the Docker image with the repository URI of the AWS Elastic Container Registry (ECR).
2. Log in to the ECR using AWS CLI.
3. Push the Docker image to the ECR repository.

## Importing Data with Flyway
1. Set up Flyway for database migration.
2. Create necessary SQL migration scripts.
3. Run Flyway to migrate data to the RDS instance.

## Creating ECS Service
1. Configure an ECS (Elastic Container Service) cluster.
2. Define task definitions for the containerized web application.
3. Create an ECS service using the task definitions.

## Creating ALB
1. Set up an Application Load Balancer (ALB) to distribute incoming traffic.
2. Configure listener rules to route traffic to the ECS service.

## Registering SSL Certificate
1. Obtain an SSL certificate from a trusted certificate authority.
2. Upload the SSL certificate to AWS Certificate Manager (ACM).

## Configuring Route 53
1. Create a hosted zone in Route 53.
2. Create a record set to map the domain to the ALB.

## Conclusion
Your web application is now fully hosted and functional on AWS. Users can access it securely using the provided domain name. Ensure to monitor the application's performance and scale resources as needed.
