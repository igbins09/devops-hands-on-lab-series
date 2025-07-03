# Lab 00 – Create EC2 Instance for Jenkins Setup
 
**Category:** Cloud Platforms

---

## Objective

Provision a virtual server (EC2 instance) on AWS to host Jenkins, which will serve as the CI server for future labs.

---

## 🔧 Tools Used

- AWS EC2 (Ubuntu 18.04 LTS)
- Git Bash (Windows) or iTerm (Mac)
- SSH Key Pair

---

## ⚙️ Steps Taken

1. Launched two Ubuntu 18.04 EC2 instances using the AWS console — one for Jenkins, one for Tomcat.
2. Configured instance type (t2.small), tags, and created a new security group allowing port 8080.
3. Created and downloaded a key pair (`.pem` file) for SSH access.
4. Connected to the instance using SSH from a local terminal:
   - Used Git Bash (Windows) or iTerm (Mac)
   - Verified permissions with `chmod 400`
   - Connected using SSH command provided by AWS
5. Verified successful connection to the EC2 environment.

---

## What I Learned

- How to provision cloud infrastructure (EC2) from the AWS console.
- How to securely connect to a remote server using SSH and key pairs.
- Basic understanding of cloud access and networking (security groups, ports).

---

## Notes

Ensure that ports 22 and 8080 are open in the security group and that the `.pem` key file has proper permissions before connecting via SSH.

---

## Next Steps

Install Java, Jenkins, Maven, and Tomcat on the EC2 instance to set up the CI environment.
