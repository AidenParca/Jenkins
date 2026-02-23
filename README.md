# Jenkins CI/CD Pipeline – Multi-Stage & Dynamic Versioning

This project demonstrates a production-style Jenkins CI/CD pipeline built as part of a DevOps bootcamp, evolving from basic Freestyle jobs to a fully scripted multi-stage Pipeline as Code workflow.

---

## Key Features

- Multi-stage Jenkins pipeline
- Dynamic application versioning per commit
- Automatic Docker image tagging per build
- Auto-publish to Docker Hub on every GitHub change
- Commit-back version increment to keep repository synchronized
- Multi-branch pipeline support
- Secure credential management inside Jenkins
- Jenkins running in Docker on DigitalOcean

---

## Pipeline Flow

1. Pull latest source code from GitHub  
2. Increment application version dynamically  
3. Commit updated version back to GitHub  
4. Build application using Maven  
5. Build Docker image with dynamic tag  
6. Push versioned image + `latest` tag to Docker Hub  

---

## ⚠ Important – Webhook Configuration

Since the pipeline commits version updates back to the repository, GitHub webhooks can trigger a build loop.

To prevent this:

- Configure GitHub webhook to ignore commits made by the Jenkins bot/email.
- Alternatively filter commits in the pipeline to skip version-update commits.

Failure to do this will cause infinite build triggering.

---

## Versions

**v1.0** – Freestyle job configured via Jenkins UI.  
**v2.0** – Scripted multi-stage pipeline using `Jenkinsfile` and `script.groovy`.

---

## Tech Stack

Jenkins • Docker • Maven • GitHub • Docker Hub • DigitalOcean • Groovy

---

## Repository

GitHub:  
https://github.com/AidenParca/Jenkins  

Docker Hub:  
https://hub.docker.com/repository/docker/aidenparca/demo-app
