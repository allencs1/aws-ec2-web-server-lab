**EC2 Web Server Project**

Overview

This project demonstrates launching and configuring a web server using Amazon EC2.

**Architecture**

User → EC2 Instance → Apache Web Server

**Services Used**
<br>
<br>
Amazon EC2 (virtual server)
<br>
<br>
Ubuntu Linux
<br>
<br>
Apache2 (web server)
<br>
<br>
**Implementation Steps**

1. Launch EC2 Instance
Selected Ubuntu AMI
Used t3.micro (free tier eligible)
Configured security group:
SSH (My IP)

2. Connect via SSH
ssh -i key.pem ubuntu@<public-ip>

3. Install Apache
sudo apt update
sudo apt install apache2 -y

4. Verify Web Server
Opened EC2 public IP in browser
Confirmed Apache default page loaded

5. Edit Web Page
cd /var/www/html
sudo nano index.html
Replaced default content with custom HTML

6. Restart Apache
sudo systemctl restart apache2
<br>
<br>

**Key Learnings**

-Launching and configuring EC2 instances

-Connecting via SSH using key pairs

-Basic Linux navigation and commands

-Installing and managing Apache web server

-Configuring security groups
<br>
<br>

**Challenges Faced**

-SSH connection confusion

-Understanding Linux file structure

-Managing permissions with sudo
<br>
<br>


**End Result**

Successfully deployed a live web server on EC2 and customized the hosted webpage.
<br>
<br>
![EC2 Instance](../screenshots/ec2-Instances.png)
![terminal](../screenshots/terminal.png)
