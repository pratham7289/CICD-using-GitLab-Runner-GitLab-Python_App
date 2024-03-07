# CICD-using-GitLab-Runner-GitLab-Python_App
This is a simple Python Flask application dockerized and configured for deployment using GitLab CI/CD.

## Prerequisites

- Docker
- GitLab CI/CD configured for Docker

## Installation

1. Clone the repository.
2. Ensure you have Docker installed and running.
3. Build the Docker image by running:
    ```bash
    docker build -t pyapp .
    ```

## Usage

- To run the Docker container locally, execute:
    ```bash
    docker run -d --name pythoncontainer -p 80:8080 pyapp
    ```
- The application will be accessible at `http://localhost`.

## Configuration

- The application reads the environment variable `NAME` to personalize the message. By default, it's set to "Mark". You can customize it by setting the environment variable accordingly.

## Continuous Integration/Continuous Deployment (CI/CD)

This project is configured for CI/CD using GitLab CI/CD. It consists of two stages:
1. **Build Stage**: Builds the Docker image.
2. **Deploy Stage**: Deploys the Docker container.

## How to Run CI/CD Pipeline

- Make sure you have access to a GitLab repository with CI/CD configured.
- Push your changes to the repository.
- GitLab CI/CD will automatically trigger the pipeline.
- Check the pipeline status in the GitLab dashboard.
