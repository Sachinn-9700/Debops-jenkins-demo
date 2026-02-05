
# 🚀 Jenkins CI/CD Demo

**`Hands-on CI/CD pipeline using Jenkins, Docker, and Kubernetes`**

This repository contains a **small DevOps demo project** that shows how a Jenkins pipeline can automate the **build, push, and deployment** of a containerized web application to Kubernetes.

---

## 🧰 Technologies Used

* **Jenkins** – Declarative CI/CD pipeline
* **Docker** – Containerization
* **Docker Hub** – Image registry
* **Kubernetes** – Deployment & Service (NodePort)
* **Apache HTTPD** – Web server
* **HTML / CSS** – Static web content

---

## ✨ Features

* Reusable Jenkins pipeline
* Automated Docker image build
* Secure Docker Hub login using Jenkins credentials
* Image push to Docker Hub
* Kubernetes deployment using `kubectl apply`
* External access via NodePort service

---

## 🔄 The Process

1. Created a simple static website
2. Containerize the application using Docker
3. Configure a Jenkins declarative pipeline
4. Store Docker credentials securely in Jenkins
5. Build and push the Docker image automatically
6. Deploy the application to Kubernetes

---

## 📘 What I Learned

* How Jenkins pipelines orchestrate CI/CD workflows
* Secure handling of credentials in Jenkins
* Docker image lifecycle from build to deployment
* Updating Kubernetes resources using manifests
* Writing readable and reusable pipelines

---

## ♻️ Reusable Pipeline Concept

The Jenkins pipeline is structured so that:

* Docker image name
* Registry credentials
* Repository details

can be changed easily, allowing the same pipeline to be reused for similar projects.

---

## 📈 Overall Growth

This project helped me:

* Strengthen my understanding of CI/CD automation
* Connect Docker and Kubernetes in a real workflow
* Improve troubleshooting and debugging skills
* Build confidence in DevOps tooling through hands-on practice

---

## ▶️ Running the Project (High-Level)

* Jenkins with Docker and kubectl installed
* Docker Hub credentials added to Jenkins
* Kubernetes cluster configured
* Run the Jenkins pipeline and access the app via NodePort

---