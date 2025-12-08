# Terraform + Ansible Lab (AWS EC2 + S3 Backend + CI/CD)

Ce projet déploie :

- Une VPC + Subnet public + Security Group
- Une instance EC2 Ubuntu avec cloud-init
- Un backend Terraform S3 + DynamoDB
- Un playbook Ansible pour configurer la VM
- Un pipeline GitHub Actions (Terraform + Ansible)

## Structure

- terraform/ : Infra AWS (EC2, VPC, SG, backend distant)
- ansible/   : Configuration de l’instance EC2
- .github/workflows/ : CI/CD

## Prérequis

- Un user IAM `terraform` avec clé d’accès
- Profil AWS CLI `terraform` configuré sur ta machine
- Bucket S3 + table DynamoDB (backend) déjà créés

## Commandes locales

```bash
cd terraform
terraform init
terraform plan
terraform apply
terraform output
