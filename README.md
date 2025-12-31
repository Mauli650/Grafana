# 📊 Grafana Stable Installation on AWS EC2 (Ubuntu)

This repository provides a **step-by-step, production-ready guide** to install
**Grafana Stable** on an **AWS EC2 Ubuntu instance**.

Ideal for:
- DevOps & Cloud Engineers
- Monitoring & Observability setups
- AWS EC2 Linux Servers
- Interview & Real-time Practice

---

## 🖥️ Environment Details

- Cloud Provider: AWS
- OS: Ubuntu (20.04 / 22.04 / 24.04)
- Architecture: x86_64
- Grafana Version: Stable

---

## 🔐 Step 1: Connect to AWS EC2 Instance

```bash
ssh -i "my-new-linux-key.pem" ubuntu@ec2-54-144-112-196.compute-1.amazonaws.com


##  Step 2: Update System Packages
sudo apt update

🔑 Step 3: Add Grafana GPG Key
sudo mkdir -p /etc/apt/keyrings
wget -q -O - https://apt.grafana.com/gpg.key \
| sudo tee /etc/apt/keyrings/grafana.asc

📦 Step 4: Add Grafana Stable Repository
echo "deb [signed-by=/etc/apt/keyrings/grafana.asc] https://apt.grafana.com stable main" \
| sudo tee /etc/apt/sources.list.d/grafana.list


📥 Step 5: Install Grafana (Stable)
sudo apt update
sudo apt install grafana -y

⚙️ Step 6: Start & Enable Grafana Service
sudo systemctl start grafana-server
sudo systemctl enable grafana-server

✅ Step 7: Verify Grafana Status
sudo systemctl status grafana-server

🌐 Step 8: Access Grafana Web UI
http://<EC2-PUBLIC-IP>:3000


