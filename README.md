
# AWS S3 Static Website Hosting

![AWS Cloud Icon](https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg)

## Project Overview

This project demonstrates how to host a **simple HTML static website** on **AWS S3**. The website contains basic HTML, CSS, and image files, and is publicly accessible via an S3 static website URL.

- **Website Type:** Static (HTML/CSS/JS)  
- **Hosting Service:** AWS S3  
- **Deployment Method:** Manual upload via AWS CLI or AWS Console  
- **Public URL:** [Visit the website](http://hosting-project-website.s3-website-us-east-1.amazonaws.com)

---

## Project Structure

DevOps-AWS-S3-Hosting/
├── CODE_OF_CONDUCT.md
├── LICENSE
├── README.md
├── index.html
├── styles/
├── images/
├── package-lock.json


- **index.html** — main page of the website  
- **styles/** — folder containing CSS files  
- **images/** — folder containing images used in the site  
- **package-lock.json** — not required for this static HTML project, can be ignored  

---

## Screenshots

> Replace these images with your actual website screenshots


![Homepage Screenshot]{<img width="1762" height="982" alt="Screenshot from 2025-10-16 13-23-55" src="https://github.com/user-attachments/assets/640d9712-fd3a-42cd-8cb6-1dfb8862283a" />}
---

## Step-by-Step Deployment Guide

### 1️⃣ Create an S3 Bucket
- Go to AWS Console → S3 → Create Bucket  
- Name your bucket (e.g., `hosting-project-website`)  
- Uncheck **Block all public access**  
- Click **Create**

### 2️⃣ Enable Static Website Hosting
- Go to **Properties → Static Website Hosting → Edit**  
- Enable static website hosting  
- Set **Index Document**: `index.html`  
- Save changes

### 3️⃣ Upload Your Files
- Using AWS CLI:
```bash
aws s3 sync . s3://hosting-project-website --acl public-read


5️⃣ Access Your Website

Visit the S3 static website URL:
http://hosting-project-website.s3-website-us-east-1.amazonaws.com



Notes

This project demonstrates manual static hosting.

For automation, you can integrate GitHub Actions or CI/CD pipelines.

No backend or server is required since it is fully static.


### AWS S3 Hosting Flow Diagram
![Uploading ChatGPT Image Oct 16, 2025, 01_04_26 PM.png…]()

