EC2 Web Server Project

## Overview
This project demonstrates launching and configuring a web server using Amazon EC2.

## Architecture
User → EC2 Instance → Apache Web Server

## Services Used
- Amazon EC2 (virtual server)
- Ubuntu Linux
- Apache2 (web server)

## Steps Performed

1. Launched EC2 Instance
- Selected Ubuntu AMI
- Used t3.micro (free tier eligible)
- Configured security group:
  - SSH (My IP)
  - HTTP (0.0.0.0/0)

2. Connected via SSH
```bash
ssh -i key.pem ubuntu@<public-ip>

3. Installed Apache
sudo apt update
sudo apt install apache2 -y

4. Verified Web Server
Accessed public IP in browser
Confirmed Apache default page loaded

5. Edited Web Page
cd /var/www/html
sudo nano index.html
Replaced default content with custom HTML

6. Restarted Apache
sudo systemctl restart apache2

Key Learnings
-How to launch and configure EC2 instances
-SSH access using key pairs
-Basic Linux navigation and commands
-Installing and managing a web server
-Security group configuration

### Challenges Faced
-SSH connection confusion
-Understanding Linux file structure
-Managing permissions with sudo

Outcome

Successfully deployed a live web server on EC2 and customized the hosted webpage.
