## Screenshots

### 1. GitHub Repository
### 2. Project Structure

Created the GitHub repository to store the Flask application, Docker configuration, tests, and CI/CD workflow.
Created the basic project structure containing the Flask application, tests, Dockerfile, requirements, and GitHub Actions workflow.

![GitHub Repository](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-13%20095121.png)

---

### 3. Flask Application

Created the Flask application with a home endpoint and a `/health` endpoint for deployment verification.

![Flask Application](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-05%20073954.png)

---

### 4. Pytest

Created automated tests for the Flask application and verified that the tests pass before deployment.

![Pytest Results](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-05%20075307.png)

---

### 5. Dockerfile

Created the Dockerfile to package the Flask application and its dependencies into a container.

![Dockerfile](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-05%20080957.png)
![Docker Build](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-05%20081008.png)

---

### 6. Docker Build

Built the Docker image locally to verify that the application can be containerized successfully.

![Docker Build](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-05%20081448.png)

---

### 7. IAM Role

Created the IAM role that allows GitHub Actions to securely access the required AWS resources.

![IAM Role](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-08%20200757.png)
![IAM Role](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-11%20082629.png)
![IAM Role](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-11%20082656.png)

---

### 8. IAM Trust Policy

Configured the trust policy to allow GitHub Actions to assume the AWS IAM role using OIDC.

![IAM Trust Policy](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-11%20082906.png)
![IAM Trust Policy](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-08%20201052.png)

---

### 9. GitHub Actions Variables

Configured the AWS role ARN as a GitHub Actions repository variable.

![GitHub Actions Variables](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-09%20012428.png)
![GitHub Actions Variables](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-11%20082947.png)

---

### 10. GitHub Actions Secrets

Configured the EC2 host and SSH private key as GitHub Actions secrets for secure EC2 deployment.

![GitHub Actions Secrets](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-08%20200229.png)
![GitHub Actions Secrets](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-09%20011623.png)

---

### 11. Amazon ECR Repository

Created the ECR repository to store the Docker image used for deployment.

![ECR Repository](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-06%20074707.png)

---

### 12. EC2 Instance

Created and configured the Amazon Linux EC2 instance that hosts the Docker container.

![EC2 Instance](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/IAM%20ROLE%20ATTACHED%20TO%20EC2.png)

---

### 13. EC2 Security Group

Configured the required inbound access for SSH and application traffic on port 5000.

![EC2 Security Group](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-14%20162916.png)

With this I was able to remove the build -
![EC2 Security Group](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-14%20162931.png)

---

### 14. GitHub Actions Workflow

Configured `cicd.yml` to automatically test, build, push, and deploy the application whenever code is pushed to the `main` branch.

https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/.github/workflows/cicd.yml

---

### 15. Docker Image in ECR

Verified that the Docker image was successfully built and pushed to the Amazon ECR repository.

![ECR Image](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-12%20113902.png)
![ECR Image](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-12%20112626.png)

---

### 16. Docker Container on EC2

Pulled the ECR image on the EC2 instance and started the Flask application inside a Docker container.

![EC2 Docker Container](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-05%20081457.png)

---

### 17. Container Logs

Checked the Docker container logs to confirm that the Flask application started successfully and was listening on port 5000.

![Container Logs](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-12%20113848.png)

---

### 18. Health Check

Tested the `/health` endpoint from the EC2 instance and received a successful healthy response.

![Health Check](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-12%20112408.png)

---

### 19. Flask Application

Verified that the deployed Flask application is accessible through the EC2 public IP address.

![Flask Application](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-12%20112311.png)

---

### 20. Successful CI/CD Pipeline

Verified that the complete GitHub Actions pipeline completed successfully from testing through deployment.

![Successful CI/CD Pipeline](https://github.com/HamidSiddiqui12/CI-CD-Pipeline-Assignment/blob/main/Snapshots/Screenshot%202026-08-12%20112113.png)
