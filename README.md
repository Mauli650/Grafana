# 📊 Grafana Tools & Commands (Stable)

This repository contains **all essential Grafana stable commands** for
installation, management, troubleshooting, plugins, and production usage.

Useful for:
- DevOps Engineers
- Cloud Engineers
- Linux Administrators
- Interview Preparation
- Real-time Server Setup (AWS / Ubuntu)

---

## 🚀 Supported OS
- Ubuntu
- Debian
- AWS EC2 Ubuntu

---

## 🔹 1. Grafana Stable Installation

```bash
sudo apt update
sudo apt install -y apt-transport-https software-properties-common wget

sudo mkdir -p /etc/apt/keyrings
wget -q -O - https://apt.grafana.com/gpg.key | sudo tee /etc/apt/keyrings/grafana.asc

echo "deb [signed-by=/etc/apt/keyrings/grafana.asc] https://apt.grafana.com stable main" \
| sudo tee /etc/apt/sources.list.d/grafana.list

sudo apt update
sudo apt install grafana -y

## **🔹 2. Grafana Service Management**

sudo systemctl start grafana-server
sudo systemctl stop grafana-server
sudo systemctl restart grafana-server
sudo systemctl enable grafana-server
sudo systemctl disable grafana-server
sudo systemctl status grafana-server

## **🔹 3. Grafana Version Check**
grafana-server -v

## **🔹 4. Grafana Update (Stable)**
sudo apt update
sudo apt upgrade grafana -y

## **🔹5. Grafana Logs & Debugging**
sudo journalctl -u grafana-server
sudo journalctl -xeu grafana-server
sudo tail -f /var/log/grafana/grafana.log

## **🔹6. Port & Network Check**
sudo ss -tulnp | grep 3000





