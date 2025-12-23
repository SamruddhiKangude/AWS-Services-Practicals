# AWS Lambda Sales Analysis Report

## 📌 Project Overview
This project demonstrates a **serverless sales reporting system** using AWS services.
A scheduled Lambda function extracts sales data from a MySQL database and sends a daily sales report via email.

---

## 🛠️ AWS Services Used
- AWS Lambda
- IAM
- Lambda Layers
- Amazon SNS
- Amazon EventBridge (CloudWatch Events)
- AWS Systems Manager (Parameter Store)
- Amazon EC2 
- CloudWatch Logs

---

## 🔄 Architecture Flow
1. EventBridge triggers the report Lambda on a schedule
2. Report Lambda fetches DB credentials from Parameter Store
3. Report Lambda invokes Data Extractor Lambda
4. Data Extractor Lambda connects and fetches sales data
5. Report Lambda formats the data
6. Report is sent via SNS email notification

---

## 🚀 Key Learnings
- IAM role-based permissions for Lambda
- Using Lambda Layers for external libraries (PyMySQL)
- VPC configuration for Lambda
- Scheduling Lambda using Cron expressions (UTC)
- Debugging Lambda using CloudWatch Logs

---

## 📧 Output
- Automated sales report sent via email
- Triggered daily (Mon–Sat) using EventBridge

---

## 📷 Screenshots
(Add screenshots of Lambda success, SNS email, and CloudWatch logs)

---

## 📚 Status
✅ Completed as part of AWS hands-on lab
