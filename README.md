# Terraform + Ansible Lab (AWS EC2 + S3 Backend + CI/CD)

Ce projet démontre la mise en place d’une infrastructure AWS automatisée
en combinant **Terraform**, **Ansible** et **GitHub Actions**.

L’objectif principal est de montrer une **approche infrastructure-as-code**
structurée, reproductible et intégrée dans une chaîne CI/CD.

---

## 🚀 Ce que déploie le projet

- Un **VPC AWS** avec :
  - un subnet public
  - un Security Group
- Une **instance EC2 Ubuntu**
  - provisionnée via **cloud-init**
- Un **backend Terraform distant**
  - S3 pour l’état
  - DynamoDB pour le verrouillage
- Un **playbook Ansible**
  - pour la configuration post-provisioning de l’instance
- Un **pipeline GitHub Actions**
  - Terraform (init / plan / apply)
  - Ansible

---

## 📁 Structure du projet



---

## 🔧 Prérequis

- Un compte AWS
- Un utilisateur IAM dédié `terraform` avec clés d’accès
- AWS CLI configuré avec un profil nommé `terraform`
- Un **bucket S3** et une **table DynamoDB** déjà créés (backend Terraform)

---

## ▶️ Commandes locales

```bash
cd terraform
terraform init
terraform plan
terraform apply
terraform output
