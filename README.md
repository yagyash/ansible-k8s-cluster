# 🚀 Kubernetes Cluster Deployment with Ansible

This project automates the deployment of a **highly available Kubernetes cluster** using **Ansible**.  
It supports multiple masters and worker nodes, with container runtime and CNI plugin (Calico) setup.

---

## 📂 Project Structure

ansible-k8s-cluster/

├── inventory/

│ └── inventory.ini # Hosts file (masters & workers)

├── playbooks/

│ ├── common.yml # Common setup for all nodes

│ ├── masters.yml # Kubernetes master setup

│ └── workers.yml # Kubernetes worker setup

├── README.md

└── .gitignore

---

## ⚙️ Requirements

- Ubuntu 24.04 / 24.04 servers (or compatible Linux)
- At least **2 CPUs & 2GB RAM per node**
- SSH access with `sudo` privileges
- Python 3 + Ansible installed on another server or on controlplane 
