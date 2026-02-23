# Jenkins CI/CD Pipeline Demo

This repository showcases a hands-on CI/CD pipeline built with Jenkins as part of a DevOps bootcamp.  
The project demonstrates the transition from UI-based job configuration to scalable, version-controlled Pipeline as Code.

---

## What I Learned

- Deploying Jenkins using Docker on a cloud server (DigitalOcean)
- Managing and versioning build tools inside Jenkins (Maven, Gradle)
- Installing and configuring tools within the Jenkins Docker container
- Securely managing and using Jenkins credentials
- Writing pipelines using Groovy (Pipeline as Code)
- Configuring and running multi-branch pipeline jobs

---

## Pipeline Workflow

The pipeline automates the following steps:

1. Pull source code from GitHub  
2. Build the application using Maven  
3. Build a Docker image  
4. Push the image to Docker Hub  

---

## Versions

**v1.0**  
Implemented using a Jenkins Freestyle job configured via the Jenkins UI.

**v2.0**  
Migrated to Pipeline as Code using a `Jenkinsfile` and `script.groovy` for a reproducible, version-controlled CI/CD workflow.

---

## Tech Stack

Jenkins • Docker • Maven • GitHub • Docker Hub • DigitalOcean

---

## Links

**GitHub Repository**  
https://github.com/AidenParca/Jenkins  

**Docker Hub Repository**  
https://hub.docker.com/repository/docker/aidenparca/demo-app
