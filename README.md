# ☁️ ROS DEPLOYMENT AND AWS EC2/S3 PROJECT
 
---

## 📦 Project 1 - Hosting a Node.js Web Application with Amazon EC2 and S3

### 🎯 Objective:
To deploy a Node.js application on an AWS EC2 instance using Ubuntu and host a dynamic image gallery using Amazon S3. The application includes a completion page that displays a personalized congratulatory message with images sourced from the S3 bucket.

---

### 🔧 Prerequisites:
- Created and configured an **IAM Role** with SSM access policies.
- Used **AWS Systems Manager Session Manager** for secure EC2 access.
- Created a **custom VPC** for isolated and secure networking.
- Used an **Ubuntu AMI (20.04)** for the EC2 instance.

---

### 🛠️ EC2 Configuration:
- Instance type: `t2.micro`
- OS: Ubuntu 20.04 LTS
- Storage: 8 GB (default)
- Installed dependencies:
  ```bash
  sudo apt update
  sudo apt install nodejs npm -y
  node -v
  npm -v
  ```
  ✅ **Screenshot taken after installation to verify versions.**

---

### 🖼️ S3 Configuration:
- Created a public S3 bucket.
- Uploaded 3+ images and made them **publicly accessible**.
- Retrieved public image URLs for use in the application.

---

### 🧾 Application Setup:
- Modified `completion.html` to:
  - Replace `[Your Name]` with my actual name.
  - Embed public URLs of S3 images in place of `S3IMAGESURL`.
- Uploaded application files via SSM to EC2 instance.
- Started the Node.js server using:
  ```bash
  node app.js
  ```

---

## 🤖 Project 2 - Deploying ROS Noetic on AWS EC2

### 🎯 Objective:
To deploy **Robot Operating System (ROS) Noetic** on a cloud-based EC2 instance. This setup supports robotic simulation development and cloud-based control via ROS tools.

---

### 🔧 Requirements:
- Instance type: `t2.micro`
- OS: Ubuntu 20.04 LTS
- Storage: 30 GB
- ROS version: **ROS Noetic**

---

### 🔍 ROS Installation Steps:

1. **Configure apt repositories:**
   ```bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   ```

2. **Add keys:**
   ```bash
   sudo apt install curl -y
   curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
   ```

3. **Update and install ROS:**
   ```bash
   sudo apt update
   sudo apt install ros-noetic-desktop-full -y
   ```

4. **Environment setup:**
   ```bash
   source /opt/ros/noetic/setup.bash
   ```

✅ **Successfully installed and sourced ROS Noetic. Ready for simulation and robotic development.**

---

## 🧠 Learnings & Skills Gained:
- Proficient in using **AWS EC2, IAM, S3, and Systems Manager**.
- Hands-on experience in **cloud-based application deployment**.
- Acquired skills in **ROS cloud deployment** and **DevOps scripting**.
- Enhanced understanding of **network isolation** via VPC.
- Practical exposure to **Ubuntu system setup, Node.js environment, and ROS tools**.

---

## 📌 Conclusion:
These projects demonstrate a comprehensive grasp of cloud-based deployment using AWS services and system-level installation of critical robotics frameworks. This experience showcases my ability to work across DevOps, cloud architecture, and software engineering disciplines effectively.
