# 🛰️ Network Monitoring & Observability Platform

This project focuses on designing and implementing an advanced **network monitoring and observability platform** using **Kubernetes**, **Docker**, **Grafana**, **Zabbix**, **PFSense**, and complementary technologies to provide real-time infrastructure visibility.

![Dashboard Preview](./assets/dashboard.png)

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Solution Architecture](#-solution-architecture)
- [Technologies Used](#-technologies-used)
- [Key Features](#-key-features)
- [Infrastructure Topology](#-infrastructure-topology)
- [Setup & Deployment](#-setup--deployment)
- [Dashboards & Metrics](#-dashboards--metrics)
- [Improvements & Next Steps](#-improvements--next-steps)
- [Author](#-author)

---

## 🌐 Overview

The goal of this project was to build a **robust, scalable, and automated platform** for real-time **network monitoring and analysis**, enabling:

- Centralized visibility of network, servers, and container health  
- Automated anomaly detection using predictive alerts  
- Intuitive visualization with custom Grafana dashboards  
- Integration with Zabbix to reduce manual intervention

---

## 🧱 Solution Architecture

The platform was designed with a **microservices-based architecture** for scalability and resilience:

- **Kubernetes** orchestrates containers and ensures high availability  
- **Docker** packages individual services  
- **Zabbix Server + Agents** collect metrics and forward data centrally  
- **Grafana** consumes data from Zabbix and provides interactive dashboards  
- **PFSense** acts as a firewall and router for segmentation and security

       ┌────────────────┐
       │    Users       │
       └──────┬─────────┘
              │
       ┌──────▼───────┐
       │   Grafana    │
       └──────┬───────┘
              │
       ┌──────▼────────┐
       │    Zabbix     │
       │   (Server)    │
       └──────┬────────┘
              │
     ┌────────▼─────────┐
     │  Agents / Hosts  │
     └──────────────────┘

---

## 🧰 Technologies Used

| Category          | Tools                          |
|--------------------|--------------------------------|
| Orchestration      | Kubernetes, Docker             |
| Monitoring         | Zabbix, Grafana               |
| Security / Network | PFSense                       |
| Languages          | Python, Shell Script          |
| Infrastructure     | Linux (Debian/Ubuntu)        |

---

## 🌟 Key Features

- 📊 **Real-time observability** with Grafana and Zabbix  
- 🔔 **Automated alerting** using triggers and escalation workflows  
- 🧠 **Scalable architecture** leveraging Kubernetes and microservices  
- 📈 **Optimized performance**, reducing manual intervention by 60%  
- 🛡️ **Enhanced infrastructure visibility** for proactive network defense

---

## 🌍 Infrastructure Topology

A simplified view of the testing environment topology:


---

## 🧰 Technologies Used

| Category          | Tools                          |
|--------------------|--------------------------------|
| Orchestration      | Kubernetes, Docker             |
| Monitoring         | Zabbix, Grafana               |
| Security / Network | PFSense                       |
| Languages          | Python, Shell Script          |
| Infrastructure     | Linux (Debian/Ubuntu)        |

---

## 🌟 Key Features

- 📊 **Real-time observability** with Grafana and Zabbix  
- 🔔 **Automated alerting** using triggers and escalation workflows  
- 🧠 **Scalable architecture** leveraging Kubernetes and microservices  
- 📈 **Optimized performance**, reducing manual intervention by 60%  
- 🛡️ **Enhanced infrastructure visibility** for proactive network defense

---

## 🌍 Infrastructure Topology

A simplified view of the testing environment topology:

[Internet]
|
[ PFSense ]
|
[ Kubernetes Cluster ]
├── Zabbix Server
├── Grafana Dashboard
├── Agents (Nodes)
└── App Containers
---

## ⚙️ Setup & Deployment

> ⚠️ Since this is an older project, the original deployment files are no longer available. The following is a **reconstructed setup guide** for reference.

### 1. Prepare the Environment
```bash
# Update packages
sudo apt update && sudo apt upgrade -y
curl -fsSL https://get.docker.com | sh
# Follow official documentation to install kubeadm, kubectl, and kubelet
sudo kubeadm init
kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml
helm repo add zabbix https://zabbix.github.io/charts/
helm install monitoring zabbix/zabbix
helm install grafana grafana/grafana
````
Import Zabbix templates for hosts and services

Connect Grafana to the Zabbix data source

Import custom JSON dashboards

📈 Dashboards & Metrics

The dashboards include:

UTC time and overall status

Zabbix cluster health

Detected problems by severity

Real-time CPU and memory usage

TPS and network traffic

Value cache metrics and anomaly detection


👤 Author

This project was developed as part of a network monitoring and observability lab for study and practical implementation purposes.

🔗 LinkedIn
 | GitHub
