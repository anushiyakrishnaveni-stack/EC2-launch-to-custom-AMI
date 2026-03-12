# AWS-Tomcat-AMI-Deployment

A step-by-step guide to deploying an Apache Tomcat 10 Web Server on AWS EC2 and creating a custom Amazon Machine Image (AMI) for rapid scaling.

## 📌 Project Overview
The goal of this project was to set up a functional Java web environment and capture its state to create a "Golden Image." This ensures that any future instances launched from this AMI will have Tomcat 10 pre-installed and configured by default.

## 🛠️ Tech Stack
* **Cloud Provider:** AWS (Amazon Web Services)
* **Service:** EC2 (Elastic Compute Cloud)
* **Operating System:** Ubuntu 24.04 LTS
* **Web Server:** Apache Tomcat 10
* **Security:** AWS Security Groups (Port 8080)

## 🚀 Step-by-Step Implementation

### 1. Instance Launch & Connection
* Launched an Ubuntu EC2 instance in the `ap-southeast-2` (Sydney) region.
* Connected to the instance via **EC2 Instance Connect**.

### 2. Tomcat 10 Installation
```bash
sudo apt-get update
sudo apt-get install tomcat10
sudo systemctl enable tomcat10
sudo systemctl start tomcat10
