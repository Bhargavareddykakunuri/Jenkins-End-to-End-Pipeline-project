# Jenkins-End-to-End-Pipeline-project
Automated CI/CD pipeline using Jenkins on Amazon Linux 2023 for a Java application.

# Jenkins CI/CD Project
This is an end-to-end DevOps project using:
- **AWS EC2 (Amazon Linux 2023)**
- **Jenkins**
- **Docker**
- **Java Spring Boot**


# 🚀 End-to-End Java CI/CD Pipeline on AWS

This project demonstrates a fully automated **Continuous Integration and Continuous Deployment (CI/CD)** pipeline using **Jenkins**, **Docker**, and **Java Spring Boot**, hosted on **Amazon Linux 2023 (AWS EC2)**.

---

## 🛠 Tech Stack
* **Application:** Java 17, Spring Boot, Maven, H2 Database (In-Memory)
* **Infrastructure:** AWS EC2 (Amazon Linux 2023)
* **CI/CD Tool:** Jenkins (Declarative Pipeline)
* **Containerization:** Docker
* **Source Control:** GitHub

---

## 🏗 Architecture Flow
1.  **Code Push:** Developer pushes Java code to GitHub.
2.  **Jenkins Trigger:** Jenkins pulls the latest code from the `main` branch.
3.  **Build Stage:** Maven compiles the code and generates a `.jar` artifact.
4.  **Containerise:** Jenkins builds a Docker image using the provided `Dockerfile`.
5.  **Deploy:** Jenkins stops any existing container and runs a new one on **Port 8081**.

---

## 📂 Project Structure
```text
.
├── src/main/java/com/example/  # Spring Boot REST API (CRUD)
├── pom.xml                     # Maven Dependencies & Build Config
├── Dockerfile                  # Instructions for Docker Image
├── Jenkinsfile                 # CI/CD Pipeline as Code
└── README.md                   # Documentation
