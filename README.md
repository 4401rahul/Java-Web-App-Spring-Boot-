# 🚀 Java CI Pipeline using Jenkins, Maven & Docker

## 📌 Project Overview

This project demonstrates a complete **Continuous Integration (CI) pipeline** built using Jenkins.
The pipeline automates the process of:

* Pulling source code from GitHub
* Building the application using Maven
* Creating a Docker image
* Pushing the image to Docker Hub

---

## 🧱 Tech Stack

* **Jenkins** – CI/CD automation tool
* **GitHub** – Source code repository
* **Maven** – Build & dependency management
* **Docker** – Containerization
* **Docker Hub** – Image registry
* **Java (Spring Boot)** – Application

---

## 🔄 CI Pipeline Flow

```
GitHub → Jenkins → Maven Build → Docker Build → Docker Hub
```

---

## ⚙️ Jenkins Pipeline Stages

### 1️⃣ Clean Workspace

* Removes old files from previous builds
* Ensures clean build environment

### 2️⃣ Clone Code

* Pulls latest code from GitHub repository
* Uses secure credentials for authentication

### 3️⃣ Build with Maven

* Runs:

  ```
  mvn clean package
  ```
* Generates executable `.jar` file

### 4️⃣ Build Docker Image

* Uses Dockerfile to containerize the application
* Tags image with Jenkins build number

### 5️⃣ Push Docker Image

* Authenticates with Docker Hub
* Pushes image for reuse and deployment

---

## 🐳 Docker Image

**Repository:** `rahuljoshi4/java-app`

**Example Tag:**

```
rahuljoshi4/java-app:3
```

---

## ▶️ How to Run the Application

### Pull the image:

```
docker pull rahuljoshi4/java-app:3
```

### Run the container:

```
docker run -d -p 8081:8080 rahuljoshi4/java-app:3
```

### Access:

```
http://localhost:8081
```

---

## 🔐 Credentials Management

* GitHub credentials stored securely in Jenkins
* Docker Hub credentials managed using Jenkins Credentials Manager
* No sensitive data exposed in pipeline

---

## 🧠 Key Learnings

* Building end-to-end CI pipelines
* Jenkins pipeline scripting
* Maven build lifecycle
* Docker image creation & tagging
* Debugging real-world CI failures
* Secure credential handling

---

## ⚠️ Challenges Faced

* Branch mismatch (`main` vs `master`)
* Docker base image issues
* GitHub webhook limitations in private network
* Docker permissions in Jenkins

---

## 💡 Solution Highlights

* Explicit branch configuration in Jenkins
* Switched to supported Docker base image
* Used SCM polling instead of webhook
* Fixed Docker permission issues

---

## 🎯 Outcome

Successfully built a **production-level CI pipeline** that:

✔ Automates build process
✔ Ensures consistency
✔ Enables portability using Docker
✔ Pushes versioned images to Docker Hub

---

## 🚀 Future Enhancements

* Add **SonarQube** for code quality
* Integrate **Trivy** for security scanning
* Deploy using **Kubernetes + ArgoCD**

---

## 👨‍💻 Author

**Rahul Joshi**
DevOps Engineer 🚀

---
