## Screenshots

### 1. GitHub Repository

Created the GitHub repository to store the Flask application, Docker configuration, tests, and CI/CD workflow.

![GitHub Repository](screenshots/01-github-repository.png)

---

### 2. Project Structure

Created the basic project structure containing the Flask application, tests, Dockerfile, requirements, and GitHub Actions workflow.

![Project Structure](screenshots/02-project-structure.png)

---

### 3. Flask Application

Created the Flask application with a home endpoint and a `/health` endpoint for deployment verification.

![Flask Application](screenshots/03-flask-application.png)

---

### 4. Pytest

Created automated tests for the Flask application and verified that the tests pass before deployment.

![Pytest Results](screenshots/04-pytest-results.png)

---

### 5. Dockerfile

Created the Dockerfile to package the Flask application and its dependencies into a container.

![Dockerfile](screenshots/05-dockerfile.png)

---

### 6. Docker Build

Built the Docker image locally to verify that the application can be containerized successfully.

![Docker Build](screenshots/06-docker-build.png)

---

### 7. IAM Role

Created the IAM role that allows GitHub Actions to securely access the required AWS resources.

![IAM Role](screenshots/07-iam-role.png)

---

### 8. IAM Trust Policy

Configured the trust policy to allow GitHub Actions to assume the AWS IAM role using OIDC.

![IAM Trust Policy](screenshots/08-iam-trust-policy.png)

---

### 9. GitHub Actions Variables

Configured the AWS role ARN as a GitHub Actions repository variable.

![GitHub Actions Variables](screenshots/09-github-actions-variables.png)

---

### 10. GitHub Actions Secrets

Configured the EC2 host and SSH private key as GitHub Actions secrets for secure EC2 deployment.

![GitHub Actions Secrets](screenshots/10-github-actions-secrets.png)

---

### 11. Amazon ECR Repository

Created the ECR repository to store the Docker image used for deployment.

![ECR Repository](screenshots/11-ecr-repository.png)

---

### 12. EC2 Instance

Created and configured the Amazon Linux EC2 instance that hosts the Docker container.

![EC2 Instance](screenshots/12-ec2-instance.png)

---

### 13. EC2 Security Group

Configured the required inbound access for SSH and application traffic on port 5000.

![EC2 Security Group](screenshots/13-ec2-security-group.png)

---

### 14. GitHub Actions Workflow

Configured `cicd.yml` to automatically test, build, push, and deploy the application whenever code is pushed to the `main` branch.

![GitHub Actions Workflow](screenshots/14-github-actions-workflow.png)

---

### 15. Docker Image in ECR

Verified that the Docker image was successfully built and pushed to the Amazon ECR repository.

![ECR Image](screenshots/15-ecr-image.png)

---

### 16. Docker Container on EC2

Pulled the ECR image on the EC2 instance and started the Flask application inside a Docker container.

![EC2 Docker Container](screenshots/16-ec2-docker-container.png)

---

### 17. Container Logs

Checked the Docker container logs to confirm that the Flask application started successfully and was listening on port 5000.

![Container Logs](screenshots/17-container-logs.png)

---

### 18. Health Check

Tested the `/health` endpoint from the EC2 instance and received a successful healthy response.

![Health Check](screenshots/18-health-check.png)

---

### 19. Flask Application

Verified that the deployed Flask application is accessible through the EC2 public IP address.

![Flask Application](screenshots/19-flask-application.png)

---

### 20. Successful CI/CD Pipeline

Verified that the complete GitHub Actions pipeline completed successfully from testing through deployment.

![Successful CI/CD Pipeline](screenshots/20-successful-cicd-pipeline.png)
