# 🚀 Static Website Hosting on AWS EC2 using Nginx

This project demonstrates how to deploy a static HTML website on an **AWS EC2 Linux instance** and configure **Nginx** as the web server to serve the website over HTTP.

It covers launching an EC2 instance, connecting via SSH, installing and configuring Nginx, managing Linux services, and allowing web traffic using AWS Security Groups.

---

## 📌 Project Overview

- Launch an AWS EC2 instance (Ubuntu Linux)
- Connect securely using SSH
- Install and configure Nginx
- Deploy a static HTML website
- Configure AWS Security Group for HTTP access
- Verify the website using public IP

---

## 🛠️ Tech Stack

- **Cloud:** AWS EC2  
- **Server OS:** Ubuntu Linux  
- **Web Server:** Nginx  
- **Networking:** AWS Security Groups  
- **Frontend:** HTML  

---

## ⚙️ Step-by-Step Implementation

### 1️⃣ Launch EC2 Instance
- Create EC2 instance using Ubuntu AMI
- Enable **Auto-assign Public IP**
- Download key pair

---

### 2️⃣ Connect to EC2 via SSH

```bash
ssh -i your-key.pem ubuntu@your-public-ip
```

3️⃣ Update System Packages
```bash
sudo apt update
```
4️⃣ Install Nginx
```bash
sudo apt install nginx -y
```
5️⃣ Check Nginx Status
```bash
systemctl status nginx
```

If inactive:
```bash
sudo systemctl start nginx
```
6️⃣ Deploy Website File

Move to web root directory:
```bash
cd /var/www/html
```

Edit or replace the default file:
```bash
sudo nano index.html
```

Paste your HTML code and save.

7️⃣ Configure AWS Security Group

Add the following inbound rule:

| Type | Protocol | Port | Source |
|------|----------|------|--------|
| HTTP | TCP      | 80   | 0.0.0.0/0 |


Save changes.

8️⃣ Access Website

Open browser:
```bash
http://your-public-ip
```
---
## 🎯 Learning Outcomes

  - Basic Linux server management  
  - Installing and managing services using systemctl  
  - Nginx web server configuration  
  - AWS EC2 instance deployment
  - Security group firewall configuration
  - Hosting static websites on cloud infrastructure
  
---
## 🔮 Future Improvements

  - Add HTTPS using Let's Encrypt  
  - Configure custom domain  
  - Automate deployment using CI/CD  
  - Dockerize Nginx setup  
  - Add monitoring and logging
