# AWS Jenkins CI/CD Pipeline

## 🚀Project Overview

This project demonstrates a complete CI/CD pipeline using Jenkins running on AWS EC2 to automatically build and deploy a containerized Node.js application using Docker.
When a developer pushes code to GitHub, Jenkins automatically builds the Docker image and deploys the application.

## 🛠️ Technologies Used

-AWS EC2
-Jenkins
-Docker
-GitHub
-Node.js
-Express.js

## 📊 Architecture

Developer pushes code → GitHub Repository → Jenkins Pipeline → Build Docker Image → Deploy Container → Application Running

## 📁 Project Structure

### aws-jenkins-cicd-pipeline
```text
|── app.js
├── package.json
├── Dockerfile
├── Jenkinsfile
└── README.md
```

## 🎯 Application

The application is a simple Node.js Express server with two endpoints:

/ – Displays deployment success message

/health – Returns application health status

## 🔄 CI/CD Pipeline Stages

Checkout source code from GitHub

Build Docker image

Stop any existing running container

Run new Docker container with updated image

## 🔧 Jenkins Pipeline

The Jenkins pipeline automates the build and deployment process whenever the pipeline is triggered.

### Pipeline stages include:

Build Docker Image

Stop Existing Container

Run Docker Container

## 🐳 Docker Container Deployment

The Docker container runs the Node.js application on port 3000 inside the container and is exposed on port 80 of the EC2 instance.

Access the application using:

http://EC2_PUBLIC_IP

## ⚡ Setup Instructions

1.Launch an AWS EC2 instance (Ubuntu)

2.Install Java and Jenkins

3.Install Docker

4.Clone this repository in Jenkins pipeline

5.Run the Jenkins pipeline to build and deploy the application

## ✅ Result

After successful pipeline execution, the Node.js application is deployed automatically inside a Docker container and accessible via the EC2 public IP.
