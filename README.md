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

### Build Images from Dockerfile
```bash
docker build -t nginx1 ./nginx1
docker build -t nginx2 ./nginx2
docker build -t nginx3 ./nginx3

## Push images to registry
docker push <registry>/nginx1:latest
