## 📷 Screenshots

### 🐳 Docker Build
![Docker Build](<img width="1594" height="891" alt="Screenshot 2026-04-23 105147" src="https://github.com/user-attachments/assets/fead1ec0-0445-4daa-8abd-f723a189ffa5" />
)

### 📦 ECR Repository
![ECR Repo](<img width="1916" height="884" alt="Screenshot 2026-04-23 105340" src="https://github.com/user-attachments/assets/fdb7a423-f2e8-4b00-9610-5f140ddb6ce8" />
)

### 🚀 Image in ECR
![ECR Image](<img width="1574" height="720" alt="Screenshot 2026-04-23 101116" src="https://github.com/user-attachments/assets/fd1cb219-49fa-4066-99d5-5f588f7190c3" />
)



# 🚀 Push Docker Image to AWS ECR

This is a practice project demonstrating how to build a Docker image and push it to AWS ECR.

## 🔧 Steps Performed
- Created Docker image using Dockerfile
- Created AWS ECR repository
- Authenticated Docker with AWS CLI
- Tagged Docker image
- Pushed image to AWS ECR

## 🛠️ Technologies Used
- Docker
- AWS ECR
- AWS CLI

## 📌 Commands Used

### Build Image

docker build -t my-app .


### Login to ECR

aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin <account-id>.dkr.ecr.ap-south-1.amazonaws.com


### Tag Image

docker tag my-app:latest <account-id>.dkr.ecr.ap-south-1.amazonaws.com/my-app-repo:latest


### Push Image

docker push <account-id>.dkr.ecr.ap-south-1.amazonaws.com/my-app-repo:latest


## 📷 Output
Image successfully pushed and verified in AWS ECR console.

---

📌 This project is created for practice and learning purposes.# docker-ecr-project
