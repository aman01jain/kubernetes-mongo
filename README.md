🚀 MongoDB Deployment on Kubernetes
This repository contains configurations and scripts for deploying MongoDB on a Kubernetes cluster. The deployment leverages Kubernetes StatefulSets, Persistent Volumes, and Replica Sets to ensure high availability, fault tolerance, and data persistence.

📁 Project Structure
/k8s-configs/ – YAML files for deployments, services, and persistent storage setup.
README.md – Project documentation.
🛠️ Features
Stateful Deployment: Uses StatefulSets to manage MongoDB pods with persistent identities.
Data Persistence: Configured Persistent Volumes (PVs) and Persistent Volume Claims (PVCs) to ensure data is retained across restarts.
High Availability: Set up Replica Sets for data redundancy and failover support.
Service Exposure: Exposes MongoDB services within the cluster for seamless communication.
📋 Prerequisites
Kubernetes cluster (Minikube, AKS, GKE, etc.)
kubectl CLI
Docker (for building MongoDB images if required)
🚀 Deployment Instructions
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/kubernetes-mongo.git
cd kubernetes-mongo
Apply Kubernetes configurations:
bash
Copy code
kubectl apply -f k8s-configs/
Verify MongoDB pods and services:
bash
Copy code
kubectl get pods  
kubectl get svc  
📊 Scaling & Monitoring
To scale the MongoDB pods:
bash
Copy code
kubectl scale statefulset mongo --replicas=3
Use kubectl logs to monitor the pods:
bash
Copy code
kubectl logs mongo-0
🧩 Future Enhancements
Automating backups using Kubernetes CronJobs.
Implementing MongoDB Sharding for handling large datasets.
Integrating Helm Charts for streamlined deployment.
📝 License
This project is open-source and available under the MIT License.
