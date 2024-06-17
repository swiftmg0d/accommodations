# Accommodations App


## Table of Contents
- [Description](#description)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Docker Setup](#docker-setup)
- [Kubernetes Setup](#kubernetes-setup)
- [Usage](#usage)

## Description
This project is a full-stack application designed to facilitate the discovery and booking of accommodations. Users can browse various types of rooms, view details about hosts, and manage bookings.

## Tech Stack
- **Frontend**: React.js
- **Backend**: Spring Boot
- **Database**: PostgreSQL

## Installation
Follow these steps to set up the project locally:
```bash
# Clone the repository
git clone https://github.com/swiftmg0d/accommodations.git

# Navigate to the project directory
cd accommodations

# Frontend setup
cd frontend
npm install
npm run dev

# Backend setup
cd ../backend
./mvnw spring-boot:run
```
## Docker Setup
Containerize and run the app with Docker. Modify `.env` file for custom configurations:
```bash
# Build and run Docker containers

docker compose up -d
```
## Kubernetes Setup
Deploy the app on Kubernetes. If using Docker Desktop, it's recommended to use the docker-desktop context.

For local development, you may need to update your hosts file:
Add this line to your hosts file located at `C:\Windows\System32\drivers\etc`

`127.0.0.1 accommodations.mk`
```bash
# Apply Kubernetes manifests

kubectl apply -f namespace.yaml  -f config_secret.yaml -f workloads.yaml -f service.yaml -f ingress.yaml
```

## Usage
Depending on your setup, access the app as follows:

### With Docker/Normal
- Frontend: `http://localhost:5137`
- Backend API: `http://localhost:8080/api`

### With Kubernetes
- Frontend: `http://accommodations.mk`
- Backend API: `http://accommodations.mk/api`



