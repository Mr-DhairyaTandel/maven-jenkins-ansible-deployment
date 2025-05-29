# CI/CD Pipeline for Maven Java App with Jenkins and Ansible

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline for a Java-based Maven application. Jenkins automates the build and deployment process, while Ansible handles remote deployment to a target EC2 server.

## ⚙️ Tech Stack

* Java (Maven)
* Jenkins
* Ansible
* Git/GitHub
* AWS EC2 (for deployment)

## 💠 Pipeline Workflow

1. Jenkins checks out the code from GitHub.
2. Jenkins builds the project using Maven (`compile`, `package`, `install`).
3. Jenkins executes an Ansible playbook that:

   * Connects to the target EC2 instance.
   * Creates a deployment directory.
   * Copies the built JAR file.
   * Optionally starts the application using `java -jar`.

## 📂 Project Structure

```
.
├── Jenkinsfile
├── deploy.yml                # Ansible playbook
├── inventory.ini             # Ansible inventory
├── key/jenkis-oneshot.pem    # Private key for SSH (not uploaded to GitHub)
├── src/
└── README.md
```

## 🚀 Deployment Steps

* Trigger the Jenkins pipeline manually or on code push.
* Monitor stages: Code, Build, Deploy.

## 🔐 Security

* SSH key is restricted with proper file permissions.
* `.pem` file is not exposed in version control.
* Remote access only via Jenkins automation.

## ✅ Result

Successful deployment of Maven JAR file from Jenkins to the remote target server using Ansible.

---

> **Author**: Dhairya Tandel
> **Company**: Mivaayu Technologies
