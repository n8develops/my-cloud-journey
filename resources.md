## Day 1–2: Watch AWS Crash Courses

### 1. AWS EC2 Crash Course
- [AWS EC2 Crash Course (freeCodeCamp)](https://www.youtube.com/watch?v=lZMkgOMYYIg) 

### 2. AWS S3 Crash Course
- [AWS S3 Simplified: Beginner's Tutorial with Step-by-Step Demo](https://www.youtube.com/watch?v=WNmkgz9yOp0) 


### 3. AWS IAM Crash Course
- [AWS IAM Roles and Policies Explained | Full Tutorial for Beginners](https://www.youtube.com/watch?v=xObZL_Dn02s&utm_source=chatgpt.com)



### 4. AWS CloudFormation Crash Course
- [AWS CloudFormation Tutorial for Beginners (2024)](https://www.youtube.com/watch?v=2gT1dvbppg8) 
---

### **AWS EC2 Setup Notes**

**1. What is EC2?**
- Elastic Compute Cloud (EC2) is AWS’s service for virtual servers (“instances”).
- Use cases: web hosting, app servers, development/test environments.

**2. Key EC2 Concepts**
- **AMI:** Amazon Machine Image (the OS and software template).
- **Instance Type:** Hardware profile (e.g., t2.micro for free tier).
- **Key Pair:** Used for SSH access (download .pem file and keep safe!).
- **Security Group:** Virtual firewall for your instance (control inbound/outbound traffic).
- **Elastic IP:** Static, public IP you can attach to an instance.

**3. Launching Your First EC2 Instance (Manual, Console)**
1. **Log in** to AWS Console, go to EC2.
2. Click “Launch Instance.”
3. **Name:** “dev-server-july2024”
4. **Choose AMI:** Amazon Linux 2 (free tier)
5. **Instance Type:** t2.micro (free tier)
6. **Key Pair:** Create new, download .pem file.
7. **Network Settings:**
   - Allow SSH (port 22) from your IP only (for security).
   - Add HTTP (port 80) if planning to serve web traffic.
8. **Storage:** Default (8 GB SSD is fine for now).
9. **Launch Instance** and wait for status checks.

**4. Connect to EC2 via SSH**
```bash
chmod 400 your-key.pem
ssh -i "your-key.pem" ec2-user@<EC2-Public-IP>
