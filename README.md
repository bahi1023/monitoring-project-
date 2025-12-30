# Ansible Prometheus Grafana Monitoring (RHEL)

Automated deployment of a **production-style monitoring stack** using **Ansible** on **Red Hat Enterprise Linux (RHEL)**.  
The project follows **DevOps best practices** for automation, observability, and infrastructure operations.

---

## 📖 Overview
This repository demonstrates how to deploy and operate a **complete monitoring solution** using Ansible with a focus on:
- Infrastructure as Code (IaC)
- Repeatable and idempotent automation
- Real-world DevOps and SOC monitoring practices

### Stack Components
- **Prometheus** – Metrics collection and scraping
- **Node Exporter** – Host-level system metrics
- **Grafana** – Visualization and dashboards
- **Alerting foundation** – Ready for Alertmanager integration

---

## 🏗️ Architecture

The environment is designed with **clear role separation** and **least-privilege principles**.

### Nodes
- **Control Node**
  - Ansible Master
  - Orchestrates configuration and deployment
  - Excluded from monitoring targets (best practice)

- **Prometheus Server**
  - Central metrics collection
  - Pull-based scraping from Node Exporter endpoints

- **Grafana Server**
  - Dashboards and visualization
  - Uses Prometheus as a data source

- **Node Exporter Nodes**
  - Monitored RHEL servers
  - Provide CPU, memory, disk, and network metrics

---

## 🛠️ Technologies

- Ansible
- Prometheus
- Grafana
- Node Exporter
- Red Hat Enterprise Linux (RHEL)
- systemd
- firewalld
- Git & GitHub

---

## 📁 Project Structure

ansible-prometheus-grafana-monitoring/

├── inventory/

│   └── hosts.ini

│   ├── prometheus/

│   ├── grafana/

│   └── node_exporter/

├── deploy_central_stack.yml

└── README.md
---


