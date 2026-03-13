# CI Pipeline to Build and Push Docker Image using GitHub Actions

## Project Overview

This project demonstrates how to create a Continuous Integration (CI) pipeline that automatically builds and pushes a Docker image to Docker Hub whenever code is pushed to the GitHub repository.

The pipeline is implemented using GitHub Actions and containerizes a simple Node.js application using Docker.

---

## Objective

The objective of this project is to automate the process of:

* Building Docker images
* Pushing Docker images to Docker Hub
* Integrating CI pipelines with GitHub

This reduces manual work and ensures consistent builds.

---

## Technologies Used

* Git
* GitHub
* GitHub Actions
* Docker
* Docker Hub
* Node.js
* Visual Studio Code

---

## Project Structure

```
ci-docker-pipeline
│
├── app.js
├── package.json
├── Dockerfile
│
└── .github
    └── workflows
        └── docker-pipeline.yml
```

---

## Application Description

The application is a simple Node.js server that runs on port **3000** and returns a message when accessed from the browser.

Example:

```
http://localhost:3000
```

---

## Dockerfile Explanation

The Dockerfile defines how the Docker image is built.

Steps included:

1. Use Node.js base image
2. Create working directory
3. Copy project files
4. Install dependencies
5. Expose port 3000
6. Run the Node.js application

---

## CI Pipeline Workflow

Whenever code is pushed to GitHub:

1. GitHub Actions workflow is triggered
2. The repository code is checked out
3. Docker image is built using Dockerfile
4. Docker Hub login is performed using GitHub Secrets
5. The image is pushed to Docker Hub

Workflow location:

```
.github/workflows/docker-pipeline.yml
```

---

## GitHub Secrets Used

To authenticate Docker Hub securely:

* DOCKER_USERNAME
* DOCKER_PASSWORD

These are stored in GitHub repository secrets.

---

## Docker Image

Docker images are pushed to Docker Hub repository:

```
shravanigulhane/ci-docker-pipeline
```

---

## How to Run the Project Locally

Pull the Docker image:

```
docker pull shravanigulhane/ci-docker-pipeline
```

Run the container:

```
docker run -p 3000:3000 shravanigulhane/ci-docker-pipeline
```

Open browser:

```
http://localhost:3000
```

---

## CI Pipeline Flow

```
Code Change
   ↓
Push to GitHub
   ↓
GitHub Actions Pipeline Triggered
   ↓
Docker Image Built
   ↓
Image Pushed to Docker Hub
```

---

## Outcome

This project successfully demonstrates:

* Automated Docker image building
* CI pipeline implementation
* Integration of GitHub Actions with Docker Hub
* Secure credential management using GitHub Secrets

---

## Future Improvements

Possible enhancements include:

* Add Continuous Deployment (CD)
* Deploy container to Kubernetes
* Add automated testing stage
* Implement Docker image version tagging

---

## Author

Shravani Gulhane
