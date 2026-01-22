# AWS IAM Hands-On Demo (Users, Groups & Roles)

## Step-by-Step Practical Implementation

### 1. Open AWS IAM Service
- Log in to the AWS Management Console.
- Search for **IAM** in the AWS search bar and open the IAM dashboard.

### 2. Create a New IAM User
- Navigate to **Access management → Users**.
- Click **Create user**.
- Enter the username: `Sam_Kangude`.
- Enable **AWS Management Console access**.
- Proceed to the next step.

### 3. Create an IAM Group and Assign Permissions
- On the permissions page, select **Create group**.
- Name the group: `employees`.
- Attach the AWS-managed policy **ViewOnlyAccess**.
- Create the group and add the user to this group.
- This allows centralized permission management for all employees.

### 4. Review IAM Policies
- Explore the difference between **AWS-managed policies** and **Customer-managed policies**.
- View the policy JSON to understand the permissions granted by `ViewOnlyAccess`.

### 5. Create an IAM Role for Temporary Access
- Navigate to **Access management → Roles**.
- Click **Create role**.
- Select **AWS account** as the trusted entity type.
- Enable **MFA** for enhanced security.

### 6. Attach Permissions to the Role
- Search for and attach the following policies:
  - `AmazonS3ReadOnlyAccess`
  - `AmazonS3TablesReadOnlyAccess`

### 7. Finalize the Role
- Name the role: `s3_read_only`.
- Review the configuration and create the role.

## Key Outcome
This setup demonstrates how to:
- Manage permissions efficiently using IAM groups
- Apply the principle of least privilege
- Use IAM roles for secure, temporary access to AWS resources like Amazon S3

This hands-on exercise strengthens understanding of AWS IAM best practices for security and scalability.
