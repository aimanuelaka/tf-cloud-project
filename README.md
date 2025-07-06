# tf-cloud-project

# 🚀 DevSecOps Infrastructure with Terraform, AWS, Docker, Jenkins, and Trivy

Ce projet met en œuvre une infrastructure DevSecOps automatisée en utilisant **Terraform** pour le provisioning sur **AWS**, **Docker** pour le packaging applicatif, **Jenkins** pour l'intégration et le déploiement continus (CI/CD), **Trivy** pour la sécurité des images, **S3** pour le stockage des artefacts et **DynamoDB** pour la gestion de l'état distant Terraform.

---

## 📦 Technologies utilisées

- **Terraform** : Infrastructure as Code (IaC)
- **AWS** :
  - EC2 (VM Jenkins)
  - S3 (Stockage des artefacts)
  - IAM (Sécurité)
  - DynamoDB (Remote backend Terraform)
- **Docker** : Conteneurisation de l’application
- **Jenkins** : CI/CD automatisé
- **Trivy** : Analyse de vulnérabilité des images Docker

---

## 🧱 Architecture

```text
Développeur ➝ Git ➝ Jenkins ➝ Docker ➝ Trivy ➝ AWS EC2/S3
                           ⬑     ⬐
                        Terraform (backend: S3 + DynamoDB)

