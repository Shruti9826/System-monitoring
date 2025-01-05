# System-monitoring
![image](https://github.com/user-attachments/assets/8e7ff0a3-c4dc-4c88-8cf9-79dac6c01db0)
This repository contains configurations and setup instructions for a **System Health Monitoring Dashboard** using **Grafana**, **InfluxDB**, and **Telegraf**.

## Features

- **Live Monitoring**:
  - Memory Utilization
  - CPU Utilization
  - Disk Usage
  - System Uptime
  - Number of Running Processes
- Configured with **Telegraf** for seamless metric collection.
- Prebuilt dashboard for visualization in **Grafana**.

---

## Setup Instructions

### Prerequisites

- Linux-based system
- Telegraf, InfluxDB, and Grafana installed
- Basic command-line knowledge

---

### Step 1: Install and Configure Telegraf

1. **Install Telegraf**:
   
     ``- For CentOS/RHEL:
     ```bash
     sudo yum install telegraf
     ```

2. **Enable and Start Telegraf**:
   ```bash
   sudo systemctl enable telegraf
   sudo systemctl start telegraf
   
### Step 2: Install and Configure InfluxDB
Install InfluxDB: Follow the InfluxDB installation guide.

Set Up the Database:

bash
Copy code
influx
> CREATE DATABASE system_health;
> CREATE USER admin WITH PASSWORD 'password';

### Step 3: Install and Configure Grafana
Install Grafana: Follow the Grafana installation guide.

Add InfluxDB as a Data Source:

URL: http://localhost:8086
Database: system_health
Username: admin
Password: password
