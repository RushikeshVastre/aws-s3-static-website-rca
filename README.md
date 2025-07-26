# 📦 AWS S3 Static Website Hosting – Downtime RCA Simulation

## 📝 Project Overview

This project demonstrates how to host a static website using **Amazon S3** and simulate downtime for **Root Cause Analysis (RCA)**.  
It’s part of my Cloud Support learning journey to build skills around real-world troubleshooting and cloud service handling.

---

## ⚙️ Tech Stack

- **AWS S3**
- **Static Website Hosting**
- **HTML**
- **GitHub**


---

## 🚀 Implementation Steps

### ✅ Step 1: Created HTML Files
- `index.html` – Homepage content  
- `error.html` – Custom error page for 4XX errors

📸 *Screenshot: index and error HTML creation*

---

### ✅ Step 2: Created S3 Bucket
- Bucket Name: `my-static-site-project`  
- Disabled “Block All Public Access”

📸 *Screenshot: Bucket settings*

---

### ✅ Step 3: Uploaded Website Files
- Uploaded both `index.html` and `error.html` directly into the bucket

📸 *Screenshot: Upload interface*

---

### ✅ Step 4: Enabled Static Website Hosting
- Enabled "Static website hosting"
- Set index document: `index.html`
- Set error document: `error.html`

📸 *Screenshot: Static website hosting enabled*

---

### ✅ Step 5: Updated Bucket Policy
- Granted public `GetObject` permission using a bucket policy

📸 *Screenshot: Policy editor with JSON*

---

### ✅ Step 6: Tested Website URL
- Opened S3 endpoint in browser
- Website loaded successfully  
👉 `http://<your-bucket-name>.s3-website-<region>.amazonaws.com`

📸 *Screenshot: Working website*

---

## ⚠️ Simulated Downtime for RCA

### 🧪 Scenario
- Manually removed public access / deleted `index.html`
- Tried accessing the site via public URL

### 🔍 Observed
- HTTP 403 or 404 errors
- Custom error page shown as expected

### 📋 RCA Report

| **Component** | **Cause**                         | **Resolution**                         |
|---------------|-----------------------------------|----------------------------------------|
| S3 Bucket     | File deleted / Access blocked     | Re-uploaded file / Updated policy      |
| Public Access | Misconfigured policy or blocked   | Reviewed and updated bucket permissions |
| Hosting Setup | Missing or wrong config           | Validated index & error document setup |

📸 *Screenshot: Error screen and resolution*

---

## 📚 Learnings

- Hosting a static site on AWS S3
- Importance of public access configuration
- Using error documents to simulate real downtime
- Writing an RCA report like a cloud support engineer

---

## 🔮 What’s Next?

- Add CloudWatch logging for request tracking
- Automate setup with Terraform
- Monitor site health using AWS Route 53 or Lambda Alerts

---

## 🤝 Connect with Me

If you're interested in collaborating on Cloud Security or Support projects, feel free to connect!

📂 **GitHub Repo**: [your-repo-link-here]  
🧑‍💻 **LinkedIn**: [your-linkedin-url]
