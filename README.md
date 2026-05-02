# 🚀 Terraform AWS EKS Cluster

## 📌 Overview

This project provisions a production-ready Amazon EKS (Elastic Kubernetes Service) cluster using Terraform.

It includes:

* Custom VPC with public and private subnets
* Managed EKS cluster with autoscaling nodes
* Secure networking using NAT Gateway
* Kubernetes NGINX deployment with LoadBalancer

---

## 🧰 Tech Stack

* Terraform
* AWS (EKS, VPC, EC2, IAM)
* Kubernetes
* kubectl

---

## 🏗️ Architecture

* VPC with 2 public and 2 private subnets
* NAT Gateway for outbound internet access
* EKS cluster deployed in private subnets
* LoadBalancer service exposed via public subnet

---

## 📁 Project Structure

terraform-aws-eks-cluster/
├── providers.tf
├── variables.tf
├── vpc.tf
├── eks.tf
├── outputs.tf
├── terraform.tfvars
└── k8s/nginx-deployment.yaml

---

## ⚙️ Prerequisites

* AWS CLI configured
* Terraform installed
* kubectl installed

---

## 🚀 Deployment Steps

### Initialize Terraform

terraform init

### Plan

terraform plan

### Apply

terraform apply

---

## 🔑 Configure kubectl

aws eks update-kubeconfig 
--region ap-south-1 
--name terraform-aws-eks-cluster

---

## 📦 Deploy Application

kubectl apply -f k8s/nginx-deployment.yaml

---

## 🌐 Access App

kubectl get svc nginx-service

---

## 🧹 Cleanup

kubectl delete -f k8s/nginx-deployment.yaml
terraform destroy

---

## 🔐 Security Highlights

* Worker nodes in private subnets
* Controlled internet access via NAT Gateway
* IAM roles managed by EKS module

---

## 📚 Key Learnings

* Infrastructure as Code (Terraform)
* AWS EKS deployment
* Kubernetes workload deployment
* VPC networking

---

## 👨‍💻 Author

Vishal Khairnar
DevOps Engineer
