## Task 2 creation of security group
## security group
security group is a virtual firewall and control inbound and outbound traffic for AWS resources. 

## ✅ Step 1: Login to AWS Console
1. Open the AWS Management Console  
2. Sign in with your AWS account  
3. Select a region 

---

## ✅ Step 2: Open EC2 Dashboard
1. Search for **EC2** in the AWS search bar  
2. Click **EC2**  
3. In the left menu, click **Security Groups**



---

## ✅ Step 3: Create Security Group
1. Click **Create security group**
2. Enter:
   - **Security group name**: `web-sg`
   - **Description**: Security group for web server
   - **VPC**: Select default VPC
---

## ✅ Step 4: Add Inbound Rules
Click **Add inbound rule** and configure:

| Type | Protocol | Port | Source |
|----|----|----|----|
| SSH | TCP | 22 | My IP |
| HTTP | TCP | 80 | 0.0.0.0/0 |

---

## ✅ Step 5: Configure Outbound Rules
- Default rule: **Allow all outbound traffic**
- Keep it unchanged (recommended)



---

## ✅ Step 6: Create Security Group
1. Click **Create security group**
2. Security group is successfully created 🎉




