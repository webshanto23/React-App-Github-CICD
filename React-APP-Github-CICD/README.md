# Vite React App with TypeScript & shadcn/ui

A modern, TypeScript-based React application built with **Vite** and **shadcn/ui** components, optimized for **fast builds**, **scalable architecture**, and **Dockerized deployment**.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
   - [Running Locally](#running-locally)
5. [Docker Setup](#docker-setup)
6. [CI/CD Pipeline](#cicd-pipeline)
7. [Project Structure](#project-structure)
8. [Environment Variables](#environment-variables)
9. [Contributing](#contributing)
10. [License](#license)

---

## Project Overview

This project demonstrates a **modern frontend architecture** using:

- **React + TypeScript**: Strong typing for safer, scalable code
- **Vite**: Lightning-fast build and dev server
- **shadcn/ui**: Component library with Tailwind CSS support
- **Docker**: Containerized builds for production
- **GitHub Actions CI/CD**: Automated build, test, and Docker image push

The app is fully production-ready with **Docker multi-stage builds**, making deployments fast and reproducible.

---

## Features

- TypeScript-first React app
- Alias path support: `@/*` → `src/*`
- Tailwind CSS integration
- shadcn/ui component library
- SPA-ready static build
- Dockerized for easy deployment
- CI/CD pipeline with GitHub Actions

---

## Tech Stack

- **Frontend**: React 18, TypeScript, Vite, shadcn/ui, Tailwind CSS
- **Build/Package**: Node.js, npm
- **Containerization**: Docker, Nginx
- **CI/CD**: GitHub Actions

---

## Getting Started

### Prerequisites

- Node.js >= 20
- npm >= 9
- Docker (for production build)

### Installation

```bash
# Clone the repository
git clone https://github.com/<username>/<repo>.git
cd <repo>

# Install dependencies
npm ci
# Start development server
npm run dev

# Build Docker Image
docker build -t vite-react-app .
docker run -p 8080:80 vite-react-app
Visit: http://localhost:8080

Note: dist/ is generated automatically by npm run build and copied to Nginx in Docker.

CI/CD Pipeline

Automated build and type-check on push to main

Docker image built and pushed to Docker Hub automatically

Tagged with both latest and commit SHA for rollback

Secrets required in GitHub Actions:
DOCKERHUB_USERNAME
DOCKERHUB_TOKEN

#Project Structure
my-app/
├── Dockerfile              # Multi-stage Dockerfile for production
├── package.json            # Node scripts & dependencies
├── tsconfig.json           # TypeScript configuration
├── vite.config.ts          # Vite configuration
├── index.html
├── src/
│   ├── main.tsx            # Entry point
│   ├── App.tsx             # Root app component
│   └── components/         # shadcn/ui components
├── .github/workflows/
│   └── ci-cd.yml           # GitHub Actions CI/CD pipeline

#Add environment variables in a .env file for Vite:
VITE_API_URL=https://api.example.com
```
