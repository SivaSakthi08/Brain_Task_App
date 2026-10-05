DevOps Practice Project – Dist Directory

This repository contains the production-ready build files (dist folder) for DevOps practice and deployment exercises.

It is intentionally structured to help learners focus on CI/CD pipelines, hosting, containerization, and infrastructure setup rather than application development.

📁 What This Repository Contains

dist/ – Compiled and production-ready static files

HTML

CSS

JavaScript

Assets (images, fonts, etc.)

These files are ready to deploy to:

Web servers (Nginx / Apache)

Cloud platforms (AWS S3, Azure Blob, GCP Storage)

Containerized environments (Docker + Nginx)

Kubernetes clusters

CI/CD pipeline demonstrations

🎯 Purpose of This Repository

This repository is designed for:

DevOps beginners

CI/CD practice

Deployment pipeline testing

Docker & Kubernetes deployment exercises

Web server configuration practice

Reverse proxy and load balancer setup

The goal is to simulate real-world deployment scenarios using already built application files.

❓ Why is there NO package.json?

You may notice that this repository does not include:

package.json

node_modules

Source code (src/)

Build tools configuration

✅ Reason:

This repository only contains the final production build output (dist), not the development source code.

In a typical project:

Developers write source code.

The project is built using tools like:

Node.js

Webpack

Vite

React (or other frameworks)

A dist/ folder is generated.

Only the production build is deployed to servers.

This repository represents step 4 only.

Since this is already the compiled output:

No dependencies are required

No build process is required

No package.json is needed
