# 🚀 Kubernetes Cluster Deployment with Ansible

This project automates the deployment of a **highly available Kubernetes cluster** using **Ansible**.  
It supports multiple masters and worker nodes, with container runtime and CNI plugin (Calico) setup.

---

## 📂 Project Structure

ansible-k8s-cluster/

├── inventory/

│ └── inventory.ini # Hosts file (masters & workers)

├── playbooks/

│ ├── common_config.yml # Common setup for all nodes

│ ├── masters_config.yml # Kubernetes master setup

│ └── workers_config.yml # Kubernetes worker setup

│ └── cni_plugin.yml # Calico setup

├── README.md

└── .gitignore

---

## ⚙️ Requirements

- Ubuntu 24.04 / 24.04 servers (or compatible Linux)
- At least **2 CPUs & 2GB RAM per node**
- SSH access with `sudo` privileges
- Python 3 + Ansible installed on another server or on controlplane

  ## For Deployment.

- ansible-playbook -i inventory/inventory.ini playbooks/common_config.yml
- ansible-playbook -i inventory/inventory.ini playbooks/master_config.yml
- ansible-playbook -i inventory/inventory.ini playbooks/cni_plugin.yml
- ansible-playbook -i inventory/inventory.ini playbooks/worker_plugin.yml
