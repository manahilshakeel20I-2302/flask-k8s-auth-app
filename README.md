# flask-k8s-auth-app
A Flask-based authentication system deployed on Kubernetes, featuring secure user management with JWT-based password reset and Kubernetes Secrets for sensitive data handling. This project demonstrates real-world backend + DevOps practices including authentication flows and secure configuration management.

## Overview
This application provides a complete user authentication flow including signup, login, forgot password, and reset password functionality. It uses JWT tokens for secure password reset and stores sensitive configuration using Kubernetes Secrets.

## Tech Stack
- Flask (Python)
- Docker
- Kubernetes
- JWT (JSON Web Tokens)
- SQLite / Database
- Kubernetes Secrets

## Features
- User Signup and Login system
- Forgot Password functionality
- Reset Password using JWT authentication
- Secure token-based verification
- Sensitive data managed using Kubernetes Secrets
- Containerized and deployed on Kubernetes

## Kubernetes Components
- Deployment – manages application pods
- Service – exposes the application
- Secrets – stores sensitive data (e.g., secret keys, tokens)

## Getting Started

### Prerequisites
- Docker installed
- Kubernetes cluster (Minikube or cloud)
- kubectl configured

### Run the Application
Build Docker image:
```bash
docker build -t flask-auth-app .
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f secrets.yaml
kubectl get services
