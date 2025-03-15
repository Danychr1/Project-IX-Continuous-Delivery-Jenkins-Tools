# Project-IX-Continuous-Delivery-Jenkins-Tools

## Why This Project?

   In an Agile development environment, code changes happen fast - sometimes multiple times a day. Every time a developer pushes new code, it needs to be:
   
 ✅ Built and tested
 
 ✅ Packaged and deployed
 
 ✅ Verified with automated tests
 
 ✅ Approved for production
 
Doing all of this manually? That's a nightmare. It's slow, prone to errors, and creates unnecessary dependencies on Ops and Release teams.

## The Problem
  
- Frequent code changes mean more room for human error.

- Manual deployments take too long.

- Approval processes and ticketing slow everything down.

- Ops teams become a bottleneck for releases.

## The Solution: Automate Everything

Instead of relying on slow, manual processes, we automate:

 🔹 Build, Test, Deploy, and Verify - Every commit triggers this cycle.
 
 🔹 Instant Notifications - So developers can fix issues ASAP.
 
 🔹 Faster Bug Fixes - Catch errors early rather than at the last minute.
 
## Tools We Used

To make this work, we set up a Continuous Delivery (CD) pipeline using:

Jenkins - The brain of our automation.

Nexus Sonatype Repository - Manages software artifacts.

SonarQube - Checks for code quality and security issues.

Maven - Helps with building Java projects.

Git - Tracks code changes.

Slack - Sends real-time updates.

Docker - Packages applications into containers.

AWS ECR - Stores Docker images.

AWS ECS - Runs containers in the cloud.

AWS CLI - Automates AWS commands.

## What This Achieves

🚀 Faster Releases - No waiting around for approvals and manual deployments.

 💡 Quick Bug Fixes - Developers get immediate feedback.
 
 ⚡ Less Downtime - Issues are caught before they hit production.
 
 🔧 More Control - No dependency on Ops for every little change.
 
## How It Works (Step-by-Step)

      1. Connect GitHub and Jenkins
      
* Set up a GitHub Webhook so every commit triggers Jenkins.
  
* Copy the Dockerfile from the vprofile repo into our own repo.
  
* Create two Jenkinsfiles - one for staging, one for production.

      2. Set Up AWS
  
* Create an IAM role for Jenkins to access AWS resources.
  
* Set up an ECR repository to store Docker images.

      3. Configure Jenkins

* Install key plugins:

       ✅ Amazon ECR
  
       ✅ Docker Build & Publish
  
       ✅ AWS Pipeline Steps
 
* Install Docker Engine and AWS CLI on Jenkins.
  
Write a Jenkinsfile to:

Build the Docker image.

Push the image to AWS ECR.

      4. Deploy to AWS ECS
      
- Create an ECS Cluster, Task Definitions, and Services.
  
- Deploy the Docker image to ECS for staging.

- If all tests pass, promote the image to production.

## The Result?

No more waiting. No more manual steps. Just smooth, automated deployments that let developers focus on what they do best - writing great code..

Author 👨🏽‍💻: Dany Christel
