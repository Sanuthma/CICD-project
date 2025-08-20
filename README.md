# Java Maven Web Application
A hands-on Java web application project designed to explore CI/CD automation using Jenkins and Docker.
## Features
- Java web application using JSP
- Maven-based project structure for builds
- Dockerfile for containerization
- Complete Jenkins CI/CD pipeline

## Skills & Technologies Learned
- Java web development
- Maven build automation
- Docker containerization
- Jenkins pipeline creation
- CI/CD automation concepts

## Application Structure

```
src/main/webapp/
├── index.jsp          # Main landing page
├── demo.jsp           
└── WEB-INF/web.xml    
```

## Build & Run

```bash
mvn clean package
```

This creates a deployable WAR file in the `target/` directory that can be deployed to Tomcat or containerized with Docker.

## CI/CD Pipeline Experience

### Tools & Setup
- Jenkins installed on an EC2 instance
- Docker installed on the same EC2 instance

### Pipeline Implementation
1. Jenkins dashboard access at `http://your-ec2-ip:8080`
2. Required Jenkins plugins:
   - Maven Integration Plugin
   - Docker Pipeline Plugin
   - GitHub Integration Plugin

3. Created Pipeline job using the `Jenkinsfile` in this repository

4. The `Jenkinsfile` contains the complete pipeline configuration for:
   - Building the Maven project
   - Creating Docker image
   - Pushing to Docker Hub
   - Deploying the container

Application runs at: `http://your-ec2-ip:9000/<your-app-name>`
