# Multi-Nginx Project

Multi-nginx container deployed through Minikube.

## Structure

multi-nginx/
├── deployment.yaml # Kubernetes deployment
├── nginx1/
│ ├── Dockerfile
│ └── index.html
├── nginx2/
│ ├── Dockerfile
│ └── index.html
└── nginx3/
├── Dockerfile
└── index.html
