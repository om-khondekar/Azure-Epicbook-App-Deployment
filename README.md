# 📚 EpicBook Application Deployment on Microsoft Azure

## 📖 Project Overview

This project demonstrates the deployment of a **Node.js (Express.js) Book Store application** on **Microsoft Azure** using a Virtual Machine, Azure Database for MySQL Flexible Server, and Nginx Reverse Proxy.

The project follows a three-tier architecture where the application is deployed on an Azure Ubuntu Virtual Machine and connected securely to an Azure MySQL Flexible Server using private networking.

This project showcases real-world cloud deployment practices including Linux administration, Azure networking, database integration, and reverse proxy configuration.

---

# 🏗️ Solution Architecture

```
                    Internet
                        │
                        ▼
                 Azure Public IP
                        │
                        ▼
           Nginx Reverse Proxy (Port 80)
                        │
                        ▼
          Node.js Express Application
                 Running on Port 8080
                        │
                        ▼
        Azure Database for MySQL Flexible Server
                        │
                        ▼
                Private Virtual Network
```

---

# 📌 Project Objectives

- Deploy a Node.js web application on Microsoft Azure.
- Configure Azure Virtual Networking.
- Secure communication using Network Security Groups.
- Connect the application with Azure Database for MySQL.
- Configure Nginx as a Reverse Proxy.
- Host the application using the VM Public IP.

---

# 🛠️ Technologies Used

## Cloud

- Microsoft Azure
- Azure Virtual Machine
- Azure Virtual Network
- Azure Database for MySQL Flexible Server
- Network Security Groups
- Public IP

## Operating System

- Ubuntu 22.04 LTS

## Backend

- Node.js
- Express.js

## Database

- MySQL
- Sequelize ORM

## Web Server

- Nginx

## Version Control

- Git
- GitHub

---

# 📂 Project Folder Structure

```
theepicbook
│
├── config
├── db
├── models
├── public
├── routes
├── views
├── package.json
└── server.js
```

---

# 🚀 Deployment Steps

## Step 1

Created Azure Resource Group.

---

## Step 2

Created Azure Virtual Network.

Configured

- Public Subnet
- Private Subnet

---

## Step 3

Configured Network Security Groups.

### Public NSG

| Port | Purpose |
|------|----------|
|22|SSH|
|80|HTTP|

### Private NSG

|Port|Purpose|
|----|--------|
|3306|MySQL|

---

## Step 4

Created Ubuntu Virtual Machine.

Configuration

- Ubuntu 22.04 LTS
- Public IP
- SSH Authentication

---

## Step 5

Installed Required Software

- Git
- Node.js
- npm
- Nginx
- MySQL Client

---

## Step 6

Cloned Application

```bash
git clone https://github.com/pravinmishraaws/theepicbook.git
```

---

## Step 7

Created Azure Database for MySQL Flexible Server.

Configuration

- MySQL Version 8
- Burstable Compute
- 20 GB Storage
- Private Access
- Private DNS Integration

---

## Step 8

Created Database

```sql
CREATE DATABASE bookstore;
```

---

## Step 9

Imported Database Files

- BuyTheBook_Schema.sql
- author_seed.sql
- books_seed.sql

Verified database tables and records.

---

## Step 10

Updated Application Configuration

Configured

- Database Host
- Username
- Password
- SSL Connection

File Updated

```
config/config.json
```

---

## Step 11

Installed Dependencies

```bash
npm install
```

---

## Step 12

Started Application

```bash
npm start
```

Application successfully started on

```
Port 8080
```

---

## Step 13

Configured Nginx Reverse Proxy

Updated

```
/etc/nginx/sites-available/default
```

Forwarded traffic

```
Port 80
        ↓
Port 8080
```

Verified

```bash
sudo nginx -t
```

Restarted

```bash
sudo systemctl restart nginx
```

---

# 🌍 Application Access

The application is accessible through the Azure Virtual Machine Public IP.

```
http://<Public-IP>
```

---

# 📸 Screenshots

Include screenshots of:

- Azure Resource Group
- Virtual Network
- Public & Private Subnets
- Network Security Groups
- Ubuntu Virtual Machine
- Azure Database for MySQL
- SSH Connection
- Database Import
- Nginx Configuration
- Application Running
- Final EpicBook Homepage

---

# 🎯 Skills Demonstrated

- Microsoft Azure
- Azure Virtual Machine
- Azure Networking
- Azure Database for MySQL
- Virtual Network
- Network Security Groups
- Linux Administration
- Nginx Reverse Proxy
- Node.js Deployment
- MySQL Database Management
- Git & GitHub
- Application Troubleshooting
- Cloud Infrastructure Deployment

---

# 📚 Key Learning Outcomes

Through this project I learned:

- Azure Infrastructure Deployment
- Azure Virtual Networking
- Network Security Configuration
- Linux Server Management
- Database Deployment and Migration
- Reverse Proxy Configuration
- Secure Database Connectivity
- Cloud Application Deployment
- End-to-End Application Hosting
- Troubleshooting Cloud Infrastructure

---

# 👨‍💻 Author

**Om Khondekar**

Aspiring DevOps Engineer

GitHub:
https://github.com/om-khondekar

LinkedIn:
(Add your LinkedIn profile link)
