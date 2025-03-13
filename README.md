# Project-IX-Continuous-Delivery-Jenkins-Tools

## **About The Project**

Scenario

In an Agile Software Development Life Cycle (SDLC):

Developers make regular code changes.

Each commit needs to be built and tested.

Packaged software or artifacts must be deployed on a server.

Software and integration testing occurs post-deployment.

Test reports are evaluated for production deployment approval.

Problem Statement

Agile SDLC involves frequent code changes.

Manual code deployment is time-consuming.

Deployment requires task assignment, ticketing, and approvals.

Dependency on Ops, Build & Release Teams creates bottlenecks.

Solution

Automate the Build, Test, Deploy, and Test process for every commit.

Implement Continuous Integration/Continuous Delivery (CI/CD).

Notify teams of build statuses.

Fix bugs and errors immediately instead of waiting for scheduled releases.

Tools Used

Jenkins: Automation server for CI/CD.

Nexus Sonatype Repository: Artifact repository.

SonarQube: Code quality and security analysis.

Maven: Build automation tool.

Git: Source code versioning.

Slack: Notifications and communication.

Docker: Containerization platform.

AWS ECR: Elastic Container Registry for Docker images.

AWS ECS: Elastic Container Service for container orchestration.

AWS CLI: Command-line interface for AWS services.

Objectives

Fault Isolation: Quickly identify and resolve failures.

Short Mean Time to Recovery (MTTR): Faster incident resolution.

Fast Turnaround on Feature Changes: Improve deployment frequency.

Less Disruptive Deployments: Reduce downtime and risks.

Flow of Execution

1. GitHub & Jenkins Integration

Update GitHub Webhook with the new Jenkins IP.

Copy Dockerfile from vprofile repository to the project repository.

Prepare two separate Jenkinsfile for staging and production environments.

2. AWS Setup

Configure IAM roles and policies for Jenkins access.

Set up an AWS ECR repository for Docker images.

3. Jenkins Setup

Install necessary plugins:

Amazon ECR

Docker, Docker Build & Publish

Pipeline: AWS Steps

Install Docker Engine and AWS CLI on Jenkins.

Write a Jenkinsfile to:

Build the application.

Publish the Docker image to AWS ECR.

4. ECS Setup

Create an ECS Cluster.

Define ECS Task Definitions and Services.

Deploy the Docker image to the ECS Cluster.

Repeat the setup for the production ECS Cluster.

5. Promoting Docker Images to Production

Validate the staging deployment.

Promote the Docker image from staging to production upon approval.

Deploy the verified image to the production ECS Cluster.

Conclusion

This automated CI/CD pipeline significantly improves deployment efficiency, reduces manual intervention, and enhances software reliability in an Agile environment. By leveraging Jenkins, AWS, and containerization technologies, organizations can achieve faster, more secure, and more scalable software delivery.
