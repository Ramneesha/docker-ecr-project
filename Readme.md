
## 📌 Overview

This project demonstrates how to build a Docker image and push it to Amazon Elastic Container Registry (ECR). It showcases the basic workflow of containerizing an application and storing it in a secure AWS-managed container registry.

---

## 🏗️ Architecture

Local Machine → Docker → AWS CLI → AWS ECR Repository

---

## 🛠️ Tech Stack

* Docker
* AWS ECR
* AWS CLI

---

## ⚙️ Prerequisites

* AWS account
* AWS CLI configured (`aws configure`)
* Docker installed and running

---

## 🔧 Implementation Steps

### 1. Build Docker Image

```bash
docker build -t my-app .
```

### 2. Authenticate Docker with AWS ECR

```bash
aws ecr get-login-password --region ap-south-1 \
| docker login --username AWS --password-stdin <your-account-id>.dkr.ecr.ap-south-1.amazonaws.com
```

### 3. Tag Docker Image

```bash
docker tag my-app:latest <your-account-id>.dkr.ecr.ap-south-1.amazonaws.com/my-app-repo:latest
```

### 4. Push Image to AWS ECR

```bash
docker push <your-account-id>.dkr.ecr.ap-south-1.amazonaws.com/my-app-repo:latest
```

---

## 📸 Output

* Docker image successfully pushed to AWS ECR
* Verified in AWS Management Console

### 🐳 Docker Build
![Docker Build](screenshots/docker-build.png)

### 📦 ECR Repository
![ECR Repo](screenshots/ecr-image.png)

### 🚀 Image in ECR
![ECR Image](screenshots/ecr-repo.png)

---

## 📌 Key Learnings

* How Docker images are built and managed
* Authentication between Docker and AWS
* Image tagging and versioning
* Pushing images to a private cloud registry

---

## 🚀 Future Improvements

* Automate deployment using GitHub Actions (CI/CD)
* Deploy container to AWS ECS or EKS
* Add version tagging instead of `latest`

---

## 📄 License

This project is licensed under the MIT License.

---
