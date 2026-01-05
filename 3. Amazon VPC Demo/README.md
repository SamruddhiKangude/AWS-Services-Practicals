🌐 AWS VPC - Designing a Secure & Highly Available AWS VPC (Public & Private Subnets)
🔍 Overview

This guide walks through creating a custom AWS VPC with:

Public & Private subnets

Multi-AZ high availability

Internet connectivity via Internet Gateway

Secure traffic control using routing

All steps follow AWS networking best practices.

🟢 Step 1: Create a VPC

➡️ AWS Console → VPC

🔹 Resource: VPC only

🔹 Name: My VPC

🔹 IPv4 CIDR: 10.0.0.0/16

✅ Create VPC

📌 This CIDR block defines the private IP range for all resources in the VPC.

🔵 Step 2: Create Private Subnets

🛡️ Used for backend resources (no internet access)

🔸 Private Subnet 1

➡️ Subnets → Create subnet

VPC: My VPC

Name: Private-subnet-1

AZ: us-east-1a

CIDR: 10.0.1.0/24

❌ Auto-assign public IP disabled

🔸 Private Subnet 2

🔁 Repeat with:

AZ: us-east-1b

CIDR: 10.0.2.0/24

🟣 Step 3: Create Public Subnets

🌍 Used for internet-facing resources

🔸 Public Subnet 1

➡️ Create subnet

VPC: My VPC

Name: Public-subnet-1

AZ: us-east-1a

CIDR: 10.0.3.0/24

✅ Enable auto-assign public IPv4

🔸 Public Subnet 2

🔁 Repeat with:

AZ: us-east-1b

CIDR: 10.0.4.0/24

🌐 Step 4: Create & Attach Internet Gateway

➡️ Internet Gateways → Create

Name: my-ig

Attach to VPC: My VPC

📌 Allows internet communication for public subnets.

🧭 Step 5: Create Public Route Table

➡️ Route Tables → Create

Name: public-route-table

VPC: My VPC

➕ Add Route

Destination: 0.0.0.0/0

Target: Internet Gateway (my-ig)

🔗 Step 6: Associate Route Table

➡️ Subnet associations → Edit

✅ Public-subnet-1

✅ Public-subnet-2

💾 Save

✔️ Public subnets → Internet access
❌ Private subnets → No internet route

🔐 Step 7: Secure Network Traffic

🛡️ Traffic control is handled by:

🔹 Security Groups → Instance-level firewall

🔹 Network ACLs → Subnet-level firewall

🔹 CIDR blocks → Define allowed IP ranges

🏗️ Final Architecture Summary

✔️ 1 VPC
✔️ 2 Public Subnets (Multi-AZ)
✔️ 2 Private Subnets (Multi-AZ)
✔️ Internet Gateway
✔️ Public Route Table
