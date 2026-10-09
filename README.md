# Git and Docker Starter Application

This repository contains a small Python web application used to practice Git, GitHub, and Docker workflows.

## Application

The application listens on port 8000 and returns a text response when accessed over HTTP.

## Verification

The running application should be verified using an HTTP request to port 8000.

## Building the Docker Image

From the project directory, run:

```bash
docker build -t git-docker-app:test .
```

## Running the Application

Start the application in a container:

```bash
docker run -d --name app-test -p 8080:8000 git-docker-app:test
```

Verify the HTTP response:

```bash
curl http://localhost:8080
```

The response includes the application title, health status for vt224, and Docker environment information.

## Stopping and Removing the Container

```bash
docker stop app-test
docker rm app-test
```

