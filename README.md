# Sample Node.js App for CI/CD Pipeline Testing

This repository contains a simple Node.js application designed for testing CI/CD pipelines and DevSecOps tools.

The project is intentionally minimal so that CI tools can quickly build and test the application, while CD tools can deploy it using Docker or container environments.

---

## Project Purpose

This repository demonstrates a basic DevSecOps pipeline workflow.

Example pipeline:

Developer Code  
↓  
CI Tool (Build + Test)  
↓  
Build Artifact / Docker Image  
↓  
CD Tool (Deployment)  
↓  
Running Application  

The repository can be used with tools such as:

### CI Tools
- Jenkins
- GitHub Actions
- GitLab CI
- CircleCI

### CD Tools
- Argo CD
- Flux
- Spinnaker
- AWS CodeDeploy

---

### File Descriptions

| File | Description |
|-----|-------------|
| app.js | Basic Node.js server |
| test.js | Simple test script used in CI |
| package.json | Node project configuration |
| Dockerfile | Container configuration for deployment |
| Jenkinsfile | Jenkins pipeline configuration |
| ci.yml | GitHub Actions pipeline |
| .gitlab-ci.yml | GitLab CI pipeline |
| config.yml | CircleCI pipeline |

---

## Prerequisites

Install the following tools:

- Node.js
- npm
- Docker (optional for container testing)
- Git

---

## Run Application Locally

Clone the repository:
git clone https://github.com/git17615/sample-node-app.git

cd sample-node-app

Install dependencies:
npm install
Start the application:
npm start
Open in browser:
http://localhost:3000


---

# CI Pipeline Steps

Typical CI pipeline stages:

1. Checkout Code
2. Install Dependencies
3. Run Tests
4. Build Docker Image

Example commands executed by CI tools:
npm install
npm test
docker build -t sample-node-app .

---

# CI Tools Configuration

This repository includes configuration files for multiple CI systems:

| CI Tool | Config File |
|-------|-------------|
| Jenkins | Jenkinsfile |
| GitHub Actions | .github/workflows/ci.yml |
| GitLab CI | .gitlab-ci.yml |
| CircleCI | .circleci/config.yml |

Each pipeline performs the same stages to allow **comparison between CI tools**.

---

# CD Deployment Workflow

After the CI pipeline builds the artifact, a CD tool can deploy the application.

Example CD flow:

Docker Image  
↓  
CD Tool  
↓  
Deployment Environment  
↓  
Running Application  

Deployment targets can include:

- Kubernetes cluster
- Cloud server
- Container runtime

---

# Usage for DevSecOps Tool Exploration

Each team member can:

1. Select **1 CI tool**
2. Select **1 CD tool**
3. Run the pipeline
4. Observe behavior
5. Document findings using the provided templates

---

# Repository Link

https://github.com/git17615/sample-node-app

---

# License

This project is intended for **educational and DevSecOps experimentation purposes**.
