🚀 Static Website Hosting on AWS EC2 using Nginx
📌 Project Overview

Deployed a static website on an AWS EC2 instance and configured Nginx as a web server. Configured Linux server, security groups, and verified website accessibility through public IP.

🛠️ Tech Stack

AWS EC2

Linux (Ubuntu)

Nginx

Networking (Security Groups)

⚙️ Steps Performed

Launched EC2 instance

Connected via SSH

Installed Nginx

sudo apt update
sudo apt install nginx -y


Verified service:

systemctl status nginx


Added website file:

sudo nano /var/www/html/index.html


Allowed HTTP in security group

Accessed site using public IP
