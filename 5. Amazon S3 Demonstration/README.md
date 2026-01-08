# 🚀 Amazon S3: Hands-on with Object Access & Bucket Policies

This project demonstrates hands-on usage of **Amazon Simple Storage Service (Amazon S3)**, focusing on **object access through browsers** and **secure access control using bucket policies**.

---

## 📌 Objective

- Create and manage an Amazon S3 bucket
- Upload objects and organize them using folders
- Access S3 objects via a browser using Object URLs
- Configure secure access using **AWS Policy Generator**
- Understand the role of `s3:GetObject` permission

---

## 🛠 Prerequisites

- AWS Account
- Basic knowledge of AWS Management Console
- A sample `.txt` file for upload

---

## 🧩 Step-by-Step Implementation

### Step 1: Create an S3 Bucket
1. Open **AWS Management Console**
2. Search for **S3** and open the service
3. Click **Create bucket**
4. Provide a globally unique bucket name
5. Select **Region: North Virginia (us-east-1)**
6. Keep **Block Public Access enabled** initially
7. Click **Create bucket**

---

### Step 2: Create Folder Structure
1. Open the newly created bucket
2. Click **Create folder**
3. Provide a folder name
4. Keep default encryption settings
5. Click **Create folder**

---

### Step 3: Upload a `.txt` File
1. Open the created folder
2. Click **Upload → Add files**
3. Select a `.txt` file from local storage
4. Click **Upload**
5. Verify that the file appears in the folder

---

### Step 4: Access Object via Browser
1. Select the uploaded object
2. Copy the **Object URL**
3. Configure permissions to allow access
4. Open the Object URL in **Google Chrome**
5. The `.txt` file opens directly in the browser

---

### Step 5: Generate Bucket Policy (AWS Policy Generator)
1. Open **AWS Policy Generator**
2. Select **Policy Type: S3 Bucket Policy**
3. Configure the following:
   - **Effect:** Allow
   - **Principal:** AWS Account ID
   - **Action:** `s3:GetObject`
   - **ARN:** `arn:aws:s3:::bucket-name/*`
4. Generate the policy
5. Paste it into **Bucket → Permissions → Bucket Policy**
6. Save changes

---

## 🔐 Why `s3:GetObject` Matters

- Allows users to **read and open objects**
- Required for accessing files using **Object URLs**
- Enables serving files like:
  - `.txt`
  - `.pdf`
  - Images
- Essential for:
  - Static website hosting
  - Data sharing
  - Public or controlled object access

---

## 📘 Key Learnings

- Every S3 object has a unique **Object URL**
- Access depends on:
  - Block Public Access settings
  - Bucket policies
- `s3:GetObject` is mandatory for browser-based access
- Security is enforced through **least-privilege permissions**

---

## 📌 Conclusion

> In Amazon S3, access is not just about uploading files — it’s about configuring the right permissions.

This hands-on project strengthened my understanding of **S3 object access, bucket policies, and secure cloud storage practices**.

---

## 🔖 Tags

AWS, Amazon S3, Cloud Computing, Bucket Policy, DevOps, Cloud Security
