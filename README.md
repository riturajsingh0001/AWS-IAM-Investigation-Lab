
# AWS IAM Investigation Lab

This lab demonstrates how to create a limited-permission IAM user, generate activity, and investigate user actions using IAM and CloudTrail.

---

## 📌 Overview

In this lab, you will:

- Create an IAM user  
- Investigate their permissions  
- Review accessed services  
- Correlate user activity using CloudTrail  

---

## ⚙️ Prerequisites

- AWS Console access with **Administrator privileges**
- CloudTrail Event History enabled *(enabled by default in most accounts)*

---

## 🚀 Steps

---

### 🔹 Step 1 – Create Investigation User

1. Open **IAM** in AWS Console  
2. Navigate to: Users → Create user  
3. Set username: lab-iam-investigation  
4. Permissions:
   - Attach policies directly  
   - Select: AmazonS3ReadOnlyAccess  
5. Create user  

---

### 🔹 Step 2 – Generate Console Login Activity (Optional)

1. Go to IAM → Users → lab-iam-investigation → Security credentials  
2. Enable console access  
3. Login using Incognito window  
4. Open S3 → View buckets → Logout  

---

### 🔹 Step 3 – Inspect User in IAM

- Check Permissions tab  
- Check Groups tab  
- Check Access Advisor tab  

---

### 🔹 Step 4 – CloudTrail Investigation

1. Open CloudTrail → Event history  
2. Filter:
   - Username: lab-iam-investigation  

3. Look for events:
   - ConsoleLogin  
   - ListBuckets  
   - GetObject  

4. Inspect:
   - eventTime  
   - sourceIPAddress  
   - userIdentity  
   - requestParameters  

---

## 🧹 Cleanup

1. IAM → Users  
2. Delete lab-iam-investigation  

---

## 💡 Learning Outcomes

- IAM permission analysis  
- Service access tracking  
- CloudTrail log investigation  
## 📄 Detailed Report

✅ The complete report has been uploaded in PDF format.
