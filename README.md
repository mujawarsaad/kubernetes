# Task 5 - Kubernetes Cluster with Minikube

## Objective

Build and manage a Kubernetes cluster locally using Minikube and deploy an application using Kubernetes Deployment and Service resources.

## Tools Used

* Minikube
* Kubernetes (kubectl)
* Docker
* Nginx

## Steps Performed

### 1. Started Minikube Cluster

Started a local Kubernetes cluster using Minikube and verified the node status.

```bash
minikube start
kubectl get nodes
```

### 2. Created Deployment

Created a Kubernetes Deployment (`deployment.yaml`) for an Nginx application with 1 replica.

```bash
kubectl apply -f deployment.yaml
```

### 3. Verified Pods

Verified that the Nginx pod was created and running successfully.

```bash
kubectl get pods
```

### 4. Exposed Application Using Service

Created a NodePort Service (`service.yaml`) to expose the Nginx application.

```bash
kubectl apply -f service.yaml
kubectl get services
```

### 5. Accessed the Application

Accessed the Nginx application using Minikube service.

```bash
minikube service nginx-service
```

### 6. Scaled the Deployment

Scaled the deployment from 1 replica to 3 replicas.

```bash
kubectl scale deployment nginx-deployment --replicas=3
```

Verified the scaling operation:

```bash
kubectl get pods
```

### 7. Inspected Deployment

Used describe command to view deployment details and troubleshooting information.

```bash
kubectl describe deployment nginx-deployment
```

## Project Files

* deployment.yaml
* service.yaml
* screenshots/

## Learning Outcomes

* Understood Kubernetes architecture and components.
* Learned how to create and manage Deployments.
* Learned how Services expose applications.
* Practiced scaling applications using Kubernetes.
* Gained hands-on experience with Minikube and kubectl commands.

## Screenshots

<image src="https://github.com/mujawarsaad/kubernetes/blob/main/image1.png">
<image src="https://github.com/mujawarsaad/kubernetes/blob/main/image2.png">
<image src="https://github.com/mujawarsaad/kubernetes/blob/main/image3.png">
