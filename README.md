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
3. Firewall & Security Configuration
OS Level: Configured UFW to allow port 8080.

Bash
sudo ufw allow 8080/tcp
AWS Level: Added a Custom TCP Rule to the Security Group for Port 8080 from anywhere (0.0.0.0/0).

**4. Verification**
Accessed the server via: http://<Public-IPv4-Address>:8080

Confirmed the "It works!" Tomcat default landing page.

**5. AMI Creation**
Captured an image of the configured instance via the AWS Console (Actions > Images and templates > Create image).

Verified the AMI status as 'Available'.

Tested the AMI by launching a new instance, which successfully served the Tomcat page without any additional configuration.

**📸 Screenshots**
(Hint: Move your uploaded screenshots into an /images folder in your repo and link them here!)

8080 port added.png - Security Group configuration.

Tomcat server.png - Successful web server response.

AMI created.png - Successful image capture in AWS.

3. Firewall & Security Configuration
OS Level: Configured UFW to allow port 8080.

Bash
sudo ufw allow 8080/tcp
AWS Level: Added a Custom TCP Rule to the Security Group for Port 8080 from anywhere (0.0.0.0/0).

4. Verification
Accessed the server via: http://<Public-IPv4-Address>:8080

Confirmed the "It works!" Tomcat default landing page.

5. AMI Creation
Captured an image of the configured instance via the AWS Console (Actions > Images and templates > Create image).

Verified the AMI status as 'Available'.

Tested the AMI by launching a new instance, which successfully served the Tomcat page without any additional configuration.

📸 Screenshots
(Hint: Move your uploaded screenshots into an /images folder in your repo and link them here!)

8080 port added.png - Security Group configuration.

Tomcat server.png - Successful web server response.

AMI created.png - Successful image capture in AWS.

🎯 Conclusion
Creating custom AMIs is a foundational DevOps practice. It reduces manual configuration errors and significantly decreases the time-to-market for deploying new application nodes.


---

**Would you like me to help you draft a specific description for your YouTube chann
Creating custom AMIs is a foundational DevOps practice. It reduces manual configuration errors and significantly decreases the time-to-market for deploying new application nodes.


---

**Would you like me to help you draft a specific description for your YouTube chann
