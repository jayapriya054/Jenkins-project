# Jenkins-project


“Automated CI/CD System with Jenkins, Docker, Kubernetes and SonarQube”


Project Overview

This project demonstrates a complete end-to-end CI/CD pipeline for a Python Flask application using Jenkins, Docker, SonarQube, and Kubernetes (k3d).


1. Automated Code Checkout

Jenkins automatically pulls source code from GitHub.

Uses secure GitHub credentials for private repositories.

2. Unit Testing

Runs pytest inside a Python Docker container.

Ensures code correctness before deployment.

3. Dependency Vulnerability Scanning

Uses Safety to detect Python package vulnerabilities.

Uses Trivy to scan Docker images for security issues.

4. Static Code Analysis (Code Review)

Integrates SonarQube for code quality analysis.

Enforces Quality Gate validation before proceeding.

5. Docker Image Build

Builds Docker image using application Dockerfile.

Tags image using Jenkins build number.

6. Docker Image Push

Authenticates securely with DockerHub.

Pushes versioned container image to registry.

7. Kubernetes Namespace Creation

Automatically creates a new preview namespace per build.

Ensures environment isolation for each deployment.

8. Application Deployment

Deploys application to Kubernetes (k3d cluster).

Exposes service using NodePort.

Generates preview URL for testing.

9. Automatic Cleanup

Schedules namespace deletion after 30 minutes.

Prevents resource leakage in cluster.

10. Consolidated Email Reporting

Sends automated email notification on success/failure.

Includes:

Number of vulnerabilities

SonarQube issues count

Docker image details

Preview URL

Sonar project link
