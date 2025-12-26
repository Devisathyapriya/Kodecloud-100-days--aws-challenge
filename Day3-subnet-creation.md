## Deleting Default Subnets in AWS VPC

### Important Note
Default subnets are created **automatically with the default VPC**.

---

## Correct Approaches

### Option 1: Delete Default Subnets (After Default VPC Exists)
1. Go to **AWS Console → VPC**
2. Click **Subnets**
3. Filter by **Default VPC**
4. Select each default subnet
5. Choose **Actions → Delete subnet**

⚠️ Subnets cannot be deleted if they are in use by EC2, NAT Gateway, or other resources.

---

### Option 2: Delete the Default VPC (Recommended)
> Deleting the default VPC automatically removes **all default subnets**.

Steps:
1. Go to **VPC → Your VPCs**
2. Select the **Default VPC**
3. Click **Actions → Delete VPC**
4. Confirm deletion

📌 AWS will recreate the default VPC automatically if needed later.

---

### Option 3: Create a Custom VPC (Best Practice)
You can simply **ignore the default VPC** and create your own.

Steps:
1. Go to **VPC → Create VPC**
2. Select **VPC only**
3. Enter CIDR block (example: `172.31.0.0/16`)
4. Create ** subnets** manually

---

## Key Points
- Default subnets belong to the **default VPC**
- Minimum subnet size in AWS is **/28**
- AWS reserves **5 IPs per subnet
