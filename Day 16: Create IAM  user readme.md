# Create an IAM User in AWS (Step-by-Step Guide)

This document explains how to **create an IAM (Identity and Access Management) user** in AWS using the **AWS Management Console**.

---

## What is an IAM User?

An **IAM User** represents a person or application that can:
- Log in to AWS
- Access AWS services
- Perform actions based on assigned permissions

IAM users are created under an AWS account and are **free of cost**.

---

## Prerequisites

- AWS account
- Login as **Root user** or an IAM user with:
  - `iam:CreateUser`
  - `iam:AttachUserPolicy`
  - `iam:CreateLoginProfile`

---

## Step 1: Login to AWS Console

1. Open **AWS Management Console**
2. Sign in with **Root user** or Admin IAM user

---

## Step 2: Open IAM Service

1. Go to **Services**
2. Search for **IAM**
3. Click **IAM**

---

## Step 3: Go to Users

1. In the left navigation panel
2. Click **Users**
3. Click **Create user**

---

## Step 4: Enter User Details

- **User name**:  
  Example: `dev-user`

- **Select AWS access type**:
  - ✅ Provide user access to the AWS Management Console (optional)
  - Console password:
    - Auto-generated or Custom password
    - Optional: Require password reset

Click **Next**

---

## Step 5: Set Permissions

Choose one of the following options:

### Option 1: Add user to group (Recommended)
- Select an existing group  
  OR  
- Click **Create group**
  - Group name: `Developers`
  - Attach required policies (e.g., `AmazonEC2ReadOnlyAccess`)

### Option 2: Attach policies directly
- Example policies:
  - `AdministratorAccess`
  - `AmazonS3FullAccess`
  - `AmazonEC2ReadOnlyAccess`

### Option 3: Copy permissions
- Copy permissions from an existing IAM user

Click **Next**

---

## Step 6: Add Tags (Optional)

Tags help with:
- Cost tracking
- User identification

Example:
```text
Key: Environment
Value: Dev
