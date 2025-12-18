🚀 Launching an EC2 Instance for a Web Server

I recently created my first EC2 web server using the AWS Management Console. Here’s a simple step-by-step breakdown of the process 👇

1️⃣ Open the EC2 Console
Log in to the AWS Management Console
Search for EC2 and open the EC2 dashboard
Click Launch Instance

2️⃣ Name Your Instance
Enter a meaningful name (example: MyInstance)
This helps identify the instance later

3️⃣ Choose an AMI (Amazon Machine Image)
Select Amazon Linux AMI
It’s lightweight, secure, and ideal for general-purpose web servers

4️⃣ Select an Instance Type
Choose t3.micro
Includes:
2 vCPU
1 GB memory
Eligible for AWS Free Tier

5️⃣ Choose a Key Pair
Select an existing key pair or create a new one (vockey)
This key pair is used for secure SSH access to the instance

6️⃣ Configure Network Settings
Keep default VPC and subnet
Enable:
✅ Allow HTTP traffic from the internet
This allows users to access the web server via browser

7️⃣ Configure Storage
Use 8 GB gp3 EBS volume
This provides enough storage for basic web content

8️⃣ Add User Data (Web Server Setup)
Scroll to Advanced Details
Under User Data, paste the script below to install and start Nginx:

```
#!/bin/bash
yum update -y
yum install nginx -y
systemctl start nginx
systemctl enable nginx
```
9️⃣ Launch the Instance
Review all settings
Click Launch Instance

🔟 Access the Web Server
Wait until the instance state shows Running
Copy the Public IPv4 address
Paste it into your browser
🎉 You should see the Nginx welcome page — your web server is live!

💡 Key Takeaways

EC2 provides flexible compute capacity in the cloud
User Data scripts automate server setup
Security groups control inbound traffic
Amazon Linux + Nginx is a great starting combo
