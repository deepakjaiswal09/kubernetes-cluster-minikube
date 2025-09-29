# 🚀 Kubernetes Deployment with Minikube

## 📌 Objective

The goal of this task is to build a local Kubernetes cluster using **Minikube**, deploy a simple Nginx application, expose it using a service, scale it, and verify logs.  


## 🛠️ Tools Used
- **Minikube** – to create the local Kubernetes cluster  
- **kubectl** – to interact with Kubernetes resources  
- **Docker** – container runtime used by Minikube  
- **VS Code** – for writing YAML manifests and running commands  

---

## 📂 Project Structure

```bash
k8s-minikube-task/
│── deployment.yaml # Deployment manifest for Nginx app
│── service.yaml # Service manifest (NodePort)
│── README.md # Documentation
```

## ⚙️ Steps Performed

## 1️⃣ Start Minikube Cluster

```bash
minikube start
kubectl get nodes
```
✅ Screenshot: Cluster node running

<img width="1920" height="1080" alt="Screenshot (1098)" src="https://github.com/user-attachments/assets/31f8d662-484a-4d22-97a0-4ac32a74409f" />


## 2️⃣ Create Deployment

Deployment manifest: deployment.yaml

```bash
kubectl apply -f deployment.yaml
kubectl get pods
```
✅ Screenshot: Pods created

<img width="1920" height="1080" alt="Screenshot (1093)" src="https://github.com/user-attachments/assets/37bc8aaf-6828-4883-81b1-a11d6e1b8f94" />

## 3️⃣ Expose Deployment with Service

Service manifest: service.yaml

```bash
kubectl apply -f service.yaml
kubectl get services
```
✅ Screenshot: Pods created

<img width="878" height="140" alt="image" src="https://github.com/user-attachments/assets/dc03256d-b51c-40c5-aae4-f4c25587b954" />

Access app in browser:

```bash
minikube service myapp-service
```
✅ Screenshot: Nginx welcome page

<img width="1920" height="1080" alt="Screenshot (1095)" src="https://github.com/user-attachments/assets/95419eb9-0e82-43ac-9847-8709aac9dd21" />

## 4️⃣ Scale Deployment

```bash
kubectl scale deployment myapp-deployment --replicas=4
kubectl get pods
```
✅ Screenshot: 4 pods running

<img width="1920" height="1080" alt="Screenshot (1097)" src="https://github.com/user-attachments/assets/646ad6d8-2c14-4f57-b9e5-d43e6ac86fc4" />

## 5️⃣ Describe Pod & Logs

```bash
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```
✅ Screenshot: Logs showing Nginx startup


<img width="1920" height="1080" alt="Screenshot (1100)" src="https://github.com/user-attachments/assets/1eb4e56f-d89b-483d-946f-4baa0be2201e" />

## ✅ Outcome

By completing this task, I learned:

-Setting up a local Kubernetes cluster
-Writing Kubernetes manifests (Deployment, Service)
-Exposing apps and accessing them in browser
-Scaling pods dynamically
-Debugging pods using logs and describe

## 🙏 Acknowledgement

I would like to express my sincere gratitude to my mentors and the DevOps Internship program for assigning Task 5: Build a Kubernetes Cluster Locally with Minikube.
This task gave me valuable hands-on experience with Kubernetes fundamentals such as creating deployments, exposing services, scaling pods, and managing logs. Completing this exercise enhanced my practical understanding of container orchestration and cluster management.
