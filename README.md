# 🚀 OpenTofu Static Website Deployment on Google Cloud

This is a self-learning project for demonstrating **Infrastructure as Code (IaC)** using **OpenTofu**, a fully open-source fork of Terraform, in combination with **Google Cloud Platform (GCP)**.

All content is original and created as part of a self-learning assignment. This project deploys a **public static website** hosted on **Google Cloud Storage**, using only OpenTofu configuration files.

## 📁 Project Structure
```
opentofu-demo/ 
    ├── main.tf # Main configuration file 
    ├── variables.tf # Input variables 
    ├── outputs.tf # Output definitions (public URL) 
    ├── index.html # Sample static website
```

## 🛠️ What This Project Does

- Creates a **Google Cloud Storage bucket**
- Enables **static website hosting**
- Uploads an **HTML file (index.html)** using OpenTofu
- Grants **public access** to all users
- Outputs the **public URL** to visit the website


## 🧱 Tools Used

- [OpenTofu](https://opentofu.org/) — open-source IaC tool
- [Google Cloud Storage](https://cloud.google.com/storage) — website hosting
- [gcloud CLI](https://cloud.google.com/sdk/docs/install) — for authentication
- HashiCorp Configuration Language (HCL)

## ✅ How to Use

### 1. Install OpenTofu and gcloud CLI
```bash
brew install opentofu/tap/opentofu         # macOS
gcloud auth application-default login
gcloud config set project YOUR_PROJECT_ID
```
### 2. Edit variables.tf or run with CLI flags:
```
tofu init
tofu plan -var="project_id=your-id" -var="bucket_name=your-unique-bucket"
tofu apply -var="project_id=your-id" -var="bucket_name=your-unique-bucket"
```
### 3. Open the output URL
```
http://your-unique-bucket.storage.googleapis.com/index.html
```

#### URL for deployed link: https://opentofu-site-eiei.storage.googleapis.com/index.html
