# DevSecOps Project: CI/CD Pipeline with Security and Monitoring

This project implements a complete DevSecOps pipeline using Jenkins for CI/CD, integrated with security scanning tools like SonarQube, OWASP Dependency-Check, Trivy, Docker image analysis, and a monitoring stack using Prometheus and Grafana. ArgoCD is used for GitOps-based deployment on a Kubernetes cluster.

---

## Architecture Diagram
![alt text](image.png)

## 🛠️ Tools & Technologies

| Category         | Tools/Services Used |
|------------------|---------------------|
| Code Repository  | GitHub              |
| CI/CD            | Jenkins             |
| Code Quality     | SonarQube           |
| Vulnerability Scanning | OWASP Dependency Check, Trivy |
| Image Scanning   | Docker Scout        |
| Container Registry | DockerHub         |
| Deployment       | Helm, ArgoCD        |
| Monitoring       | Prometheus, Grafana |
| Notification     | Gmail (email alerting) |
| Source Control   | VS Code             |

---

## 🔁 Pipeline Flow

1. **VS Code to GitHub**: Code is pushed to a GitHub repository.
2. **Jenkins Pipeline**:
    - Checks out the code.
    - Runs **SonarQube analysis** for code quality and bug detection.
    - Uses **OWASP Dependency-Check** to scan for vulnerable packages.
    - Executes **Trivy** to identify vulnerabilities in Docker images.
3. **Build and Push**:
    - Builds Docker image.
    - Pushes to **DockerHub**.
    - Scans pushed image using **Docker Scout**.
4. **Deployment**:
    - Uses **Helm** charts.
    - ArgoCD automatically pulls the Helm manifests and deploys them to Kubernetes.
5. **Monitoring & Alerts**:
    - Prometheus scrapes metrics from K8s pods.
    - Grafana visualizes the metrics.
    - Gmail notifications are triggered based on metrics/alerts.

---

## 📊 Monitoring Dashboard

- Prometheus collects pod metrics (CPU, memory, availability).
- Grafana dashboards visualize application health and alert thresholds.

---

## 🔐 Security Features

- **Code Quality Gate** via SonarQube.
- **Static Dependency Scanning** with OWASP.
- **Docker Image Vulnerability Scanning** using Trivy and Docker Scout.
- **Manual Approval Gate** before production deployment (optional).

---

## 📬 Notifications

- Gmail notifications can be configured via SMTP plugin in Jenkins or from ArgoCD Alerts.


---

## Project Documentation

Refer to this text file it has detailed documentation how to create this project.
[text](<This Project Complete Readme.txt>)

---
## SonarQube
![Screenshot (100)](https://github.com/user-attachments/assets/6d83c93c-832f-4ecd-a1b4-8042dc90eae9)

## SonarQube Webhook
![Screenshot (102)](https://github.com/user-attachments/assets/1ad9f86c-8b0f-4f75-844b-2097d1994783)

---

## Jenkins Pipeline

![Screenshot (103)](https://github.com/user-attachments/assets/3324bfc6-d552-4ba6-b217-d8c5424f0567)



---

## ArgoCd Deployment

![Screenshot (107)](https://github.com/user-attachments/assets/0683f7af-5760-4878-ba58-75c0285e06f3)

---

## Prometheus Monitoring

![Screenshot (108)](https://github.com/user-attachments/assets/cdec223c-d492-4023-96a1-e616eea65aa8)

---

## Website

![Screenshot (109)](https://github.com/user-attachments/assets/1e5ea233-ea46-4f75-95f2-acdce8589074)

## 👨‍💻 Author

Lovish Barber – [GitHub](https://github.com/lovish69)

---

## 📜 License

This project is licensed under the MIT License.
