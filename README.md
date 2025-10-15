# Multi-Nginx Project

Multi-nginx container deployed through Minikube.

## Structure

multi-nginx/<br>
├── deployment.yaml # Kubernetes deployment<br>
├── nginx1/<br>
│ ├── Dockerfile<br>
│ └── index.html<br>
├── nginx2/<br>
│ ├── Dockerfile<br>
│ └── index.html<br>
└── nginx3/<br>
├── Dockerfile<br>
└── index.html<br>

### Build & Push Images from Dockerfile

```bash
docker build -t nginx1 ./nginx1
docker build -t nginx2 ./nginx2
docker build -t nginx3 ./nginx3

## Push images to registry
docker push <registry>/nginx1:latest

### Push images to registry

docker push <registry>/nginx1:latest

### ** Deploy to Kubernetes**
kubectl apply -f deployment.yaml

### **Port Forward to Access Nginx**
kubectl port-forward pod/<pod-name> 8081:80

Open **http://localhost:8081** in your browser.
