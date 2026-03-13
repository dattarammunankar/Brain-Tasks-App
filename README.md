# 🧠 Brain-Tasks-App: DevOps Practice Project

This repository contains the production-ready build files for DevOps practice and deployment exercises. It is intentionally structured to help learners focus on **CI/CD pipelines, containerization, and Kubernetes infrastructure** rather than application development.

## 📁 What This Repository Contains
* **dist/** – Compiled and production-ready static files (HTML, CSS, JS).
* **Dockerfile** – Configuration to containerize the `dist` folder using Nginx.
* **buildspec.yml** – Automation instructions for AWS CodeBuild.
* **k8s/** – Manifest files (Deployment & Service) for Kubernetes orchestration.

These files are optimized for deployment to:
* **Containerized environments** (Docker + Nginx)
* **Kubernetes clusters** (Amazon EKS)
* **CI/CD pipeline demonstrations** (AWS CodePipeline)



---

## 🎯 Purpose of This Repository
This repository is designed for:
* **DevOps beginners** practicing cloud deployments.
* **CI/CD practice** using AWS Developer Tools.
* **Docker & Kubernetes** deployment exercises.
* **Load balancer and ingress** setup practice in EKS.

The goal is to simulate real-world deployment scenarios using already built application files.

---

## ❓ Why is there NO package.json?
You may notice that this repository does not include a `package.json`, `node_modules`, or a `src/` folder.

**✅ Reason:**
This repository only contains the **final production build output**, not the development source code. In a typical professional workflow:
1.  Developers write source code in a separate repo.
2.  The project is built using Node.js/Vite.
3.  A `dist/` folder is generated.
4.  **Only the production build (this repo) is sent to the DevOps pipeline for deployment.**

Since this is already the compiled output:
* No NPM dependencies are required.
* No local build process is required.
* The deployment is faster and more secure.

---

## 🚀 How This Project Was Deployed
1.  **Code** was pulled from GitHub via **AWS CodePipeline**.
2.  **AWS CodeBuild** used the `Dockerfile` to wrap the `dist/` folder into an Nginx image.
3.  The image was stored in **Amazon ECR**.
4.  The final app was deployed to **Amazon EKS** and made public via an **AWS Load Balancer**.
