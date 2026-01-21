# Attach an EBS Volume to an EC2 Instance (Step-by-Step Guide)

This guide explains how to **attach an existing Amazon EBS volume to an EC2 instance** and make it usable inside the OS.

---

## Prerequisites

- An **EC2 instance** in `running` or `stopped` state
- An **EBS volume** in the **same Availability Zone** as the EC2 instance
- Required IAM permissions:
  - `ec2:AttachVolume`
  - `ec2:DescribeVolumes`
  - `ec2:DescribeInstances`

---

## Step 1: Open EC2 Dashboard

1. Login to **AWS Management Console**
2. Go to **Services → EC2**
3. Click **Volumes** under **Elastic Block Store**

---

## Step 2: Select the EBS Volume

1. Choose the volume you want to attach
2. Ensure:
   - **State**: `available`
   - **Availability Zone** matches the EC2 instance

---

## Step 3: Attach the Volume

1. Select the volume
2. Click **Actions → Attach volume**
3. Choose:
   - **Instance**: Select your EC2 instance
   - **Device name**: `/dev/xvdf` (recommended)
4. Click **Attach volume**

---

## Step 4: Verify Volume Attachment

1. Go to **EC2 → Instances**
2. Select your instance
3. Scroll to **Storage**
4. Confirm volume state shows **attached**

---

## Step 5: Connect to the EC2 Instance
now successful attached instance with Volume

