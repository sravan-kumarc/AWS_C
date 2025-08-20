**EC2**

Here’s a **step-by-step guide to launch an AWS EC2 instance** (virtual server):

**1. Sign in to AWS Console**
- Go to https://aws.amazon.com
- Click **Sign In to the Console** and enter your credentials.

**2. Navigate to EC2 Dashboard**
- From the AWS Management Console, search for “EC2” and select **EC2** under Services.
- You’ll reach the EC2 Dashboard.

**3. Launch an Instance**
- Click the orange **Launch Instance** button.

**4. Name and Choose Amazon Machine Image (AMI)**
- Enter a name for your instance (e.g., MyFirstServer).
- Scroll down and choose an **AMI** (Amazon Machine Image)—for example, **Amazon Linux 2**, Ubuntu, or Windows.
- Click **Select** next to your preferred AMI.

**5. Choose Instance Type**
- Select an instance type. For most new users, **t2.micro** or **t3.micro** (eligible for Free Tier) is recommended.
- Click **Next: Configure Instance Details** (or proceed as prompted).

**6. Configure Instance Settings**
- You can leave most defaults.
- Choose the **number of instances** (usually 1).
- Optionally, configure network, subnet, IAM role, etc.

**7. Add Storage**
- Modify storage (SSD/HDD, size) if needed.
- Default (8GB GP2) is sufficient for most purposes.

**8. Add Tags**
- Add tags for organization (optional). E.g., Key: Name, Value: MyFirstServer.

**9. Configure Security Group**
- Create a new security group or use an existing one.
- Allow SSH (port 22) for Linux or RDP (port 3389) for Windows.
- Restrict source IP to your range for security (not 0.0.0.0/0 unless testing).

**10. Review and Launch**
- Review all settings.
- Click **Launch**.
- In the popup, select **Create a new key pair** (for SSH access), download the .pem file, and keep it safe.
- Acknowledge you have access to the key, and click **Launch Instances**.

**11. Access Your Instance**
- Once the instance state is “Running,” select it and note its **Public IPv4 address**.
- To SSH in (Linux):  
  ```bash
  ssh -i /path/to/your-key.pem ec2-user@<Public-IP>
  ```
- For Windows, use RDP and the credentials provided.

***

**Tips:**
- Stop/delete the instance after use to avoid charges.
- Never share your private key (.pem) file.

Want screenshots or need guidance on a specific OS (Linux/Windows)? Let me know!
<img width="961" height="541" alt="image" src="https://github.com/user-attachments/assets/3fb204db-3eb9-4265-be74-93d4a4bcabbb" />

