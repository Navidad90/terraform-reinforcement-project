# Terraform Azure Reinforcement Project

This repository demonstrates a complete, end-to-end Terraform workflow on Microsoft Azure, built as part of a structured learning and reinforcement process.

The goal of this project is not just to deploy resources, but to deeply understand **how Terraform works**, how Azure infrastructure is layered, and how to manage the full lifecycle safely in a shared tenant.

---

## What This Project Deploys

The project provisions a small but realistic Azure infrastructure stack:

- Azure Resource Group (dedicated, non-production)
- Virtual Network (VNet)
- Subnet
- Network Security Group (NSG)
- Public IP
- Network Interface (NIC)
- Linux Virtual Machine (Ubuntu)

All resources are created using Terraform and can be **fully destroyed** without impacting any existing production environments.

---

## What This Project Demonstrates

This project focuses on fundamentals rather than complexity:

- Clean Terraform project structure
- Provider and Terraform version pinning
- Implicit resource dependencies
- Network and security layering
- SSH-based VM access using RSA keys
- Safe usage of Terraform state
- Full Terraform lifecycle:
  - `init`
  - `plan`
  - `apply`
  - `destroy`

The emphasis is on **understanding and predictability**, not copy-pasting examples.

---

## Project Structure

```text
terraform-reinforcement-project/
├── main.tf
├── providers.tf
├── versions.tf
├── variables.tf
├── outputs.tf
├── .terraform.lock.hcl
├── .gitignore
└── README.md

## How to Use

Initialize Terraform:
terraform init

Review the plan:
terraform plan

Apply the infrastructure:
terraform apply

Destroy everything when finished:
terraform destroy


## Safety Notes

- Terraform state files are excluded from version control
- No secrets or private keys are stored in this repository
- All resources are deployed into a dedicated, non-production resource group
- Designed for learning and safe cleanup


## Author

Built as part of a Terraform learning journey focused on fundamentals,
discipline, and long-term understanding.
