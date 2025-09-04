# AWS DevOps CI/CD Pipeline – 7-Day Challenge

## Overview
A learning project to build an end-to-end CI/CD pipeline on AWS over seven days—from code commit to automated deploy. You'll gain hands-on experience using Java, Maven, GitHub, and AWS services like EC2, S3, CodeArtifact, CodeBuild, CodeDeploy, and CodePipeline.

## Project Structure

├── appspec.yml # AWS CodeDeploy deployment instructions
├── buildspec.yml # AWS CodeBuild build configuration
├── pom.xml # Maven build file
├── settings.xml # Maven configuration (repositories, auth)
├── scripts/ # Deployment and utility scripts (e.g., bash)
├── src/ # Application source code
└── target/ # Build artifacts (e.g., WAR file)


## Prerequisites
- Java (Corretto 8)
- Apache Maven
- AWS CLI configured (with appropriate permissions)
- Git & GitHub Personal Access Token

---

## Daily Breakdown

### Day 1 – **Initial Setup**
- Launch an EC2 instance and install Java & Maven
- Scaffold a web app using Maven archetype
- Use VS Code with Remote-SSH for development

### Day 2 – **Version Control Setup**
- Initialize Git, connect to GitHub repository
- Commit and push initial code using a GitHub token for authentication

### Day 3 – **Dependency Management via CodeArtifact**
- Create an AWS CodeArtifact repository
- Configure Maven to use CodeArtifact via `settings.xml` and IAM permissions

### Day 4 – **Continuous Integration via CodeBuild**
- Configure an S3 bucket for artifacts
- Create a `buildspec.yml` and CodeBuild project to compile and package the app

### Day 5 – **Automated Deployment via CodeDeploy**
- Write deployment scripts (e.g., to deploy WAR to Tomcat)
- Define deployment steps in `appspec.yml` and configure CodeDeploy

### Day 6 – **Infrastructure as Code (Optional)**
- (Optional) Introduce CloudFormation for provisioning EC2, IAM roles, S3, etc.

### Day 7 – **Orchestrating with CodePipeline**
- Define AWS CodePipeline integrating GitHub → CodeBuild → CodeDeploy
- Trigger a full pipeline on GitHub commits, completing the automated workflow

---

## How to Build & Deploy

**Build locally:**
```bash
mvn -s settings.xml compile
mvn -s settings.xml package

