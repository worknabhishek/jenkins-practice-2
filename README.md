# Jenkins & Ansible Automated CI/CD Pipeline

This project demonstrates a fully automated CI/CD pipeline that deploys a web application from **GitHub** to an **Apache** server using **Jenkins** for orchestration and **Ansible** for configuration management.

## 🚀 The Architecture
* **Source Control:** GitHub repository (`main` branch).
* **Orchestration:** Jenkins (Triggered by code push/webhook).
* **Configuration Management:** Ansible (Automated deployment via playbook).
* **Target:** Apache Web Server (AWS EC2).

## 🛠️ The Pipeline Workflow
1.  **Code Commit:** Changes are pushed to the GitHub repository.
2.  **CI Trigger:** Jenkins polls the repository and triggers the pipeline.
3.  **Deployment:** Jenkins executes an Ansible playbook on the target server.
4.  **Production:** The web application is updated instantly on the Apache server.

## 🚧 Challenges Solved
During the development of this pipeline, I successfully resolved:
* **SSH Integration:** Configured secure communication between Jenkins, Ansible, and the target Apache server, overcoming `Status 255` connectivity errors.
* **YAML Syntax & Logic:** Debugged Ansible task execution issues caused by indentation errors and redundant deployment steps, optimizing the build process for a "SUCCESS" status.

## 📁 Repository Structure
```text
├── jenkins-configs/    # Jenkins job configuration files
├── playbooks/          # Ansible deployment playbooks (e.g., abc.yml)
├── index.html          # Web application source code
└── README.md           # Project documentation
