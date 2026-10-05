# Brain Tasks App – DevOps Deployment

## Project Overview

Deployment of the Brain Tasks React application using Docker, Docker Hub, Kubernetes (AWS EKS), AWS CodeBuild, AWS CodePipeline, GitHub, and CloudWatch.

## Architecture

GitHub → AWS CodePipeline → AWS CodeBuild → Docker Hub → AWS EKS → Kubernetes LoadBalancer

## Application

Source Repository:
https://github.com/Vennilavanguvi/Brain-Tasks-App.git

The application is served from the production `dist` build using Nginx.

## Docker

Created a Dockerfile to serve the application using Nginx.

Run locally on port 3000:

```bash
docker build -t brain-tasks-app .
docker run -d -p 3000:80 brain-tasks-app

## Docker Hub

Docker Image:

`sivasakthi08/brain-tasks-app:latest`

## Kubernetes – AWS EKS

EKS Cluster:

`sivasakthi`

Kubernetes resources:

- `deployment.yaml`
- `service.yaml`

The deployment runs 2 application replicas.

The Kubernetes Service uses a LoadBalancer to expose the application.

## AWS CodeBuild

CodeBuild Project:

`brain-tasks-build`

The `buildspec.yml` performs:

- Docker image build
- Docker Hub push
- EKS authentication
- Kubernetes deployment
- Kubernetes service deployment

## AWS CodePipeline

Pipeline:

`brain-tasks-pipeline`

Pipeline flow:

**GitHub → CodeBuild → EKS**

The pipeline successfully builds and deploys the application to EKS.

## Monitoring

AWS CloudWatch Logs are enabled for CodeBuild to monitor build and deployment execution.

## Live Application

http://a8e23c2cf37784205b4857daa7402ca3-1977576573.ap-south-1.elb.amazonaws.com

## Repository Structure

```text
├── Dockerfile
├── buildspec.yml
├── deployment.yaml
├── service.yaml
├── dist/
└── README.md
