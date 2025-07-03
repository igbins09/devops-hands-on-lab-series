# Lab 01 – Set up Jenkins and Tomcat EC2 Instances in AWS Cloud

**Category:** CI/CD Pipelines

---

## Objective

Install and configure Jenkins and Tomcat servers on two separate EC2 instances to prepare for CI/CD and Java web app deployment.

---

## Tools Used

- AWS EC2 (Ubuntu 22.04 LTS)
- Jenkins
- Tomcat 9
- Java 11
- Maven
- Git Bash (Windows)

---

## Steps Taken

### Jenkins Server (EC2 Instance #1):
1. Created a new EC2 instance (Ubuntu 22.04) and changed its hostname to `Jenkins`.
2. Installed Java 11 using `apt` and verified it using `java -version`.
3. Installed Maven using `sudo apt install maven -y` and verified with `mvn --version`.
4. Added Jenkins repository key and installed Jenkins using `apt`.
5. Opened port 8080 in the security group to allow browser access.
6. Retrieved the initial Jenkins admin password and completed the setup wizard in the browser.

### Tomcat Server (EC2 Instance #2):
1. Created another EC2 instance for Tomcat and changed its hostname to `Tomcat`.
2. Installed Tomcat 9 and related packages using `apt`.
3. Configured admin access by editing `tomcat-users.xml` and adding a user with `manager-script` role.
4. Restarted Tomcat and confirmed it was running.
5. Verified access to the Tomcat server via the public DNS and port 8080.

---

## What I Learned

- How to provision multiple EC2 instances for different services.
- How to install and configure Jenkins and Tomcat manually.
- How to modify Linux system files and restart services.
- How to securely expose ports for web-based DevOps tools.

---

## Notes

- Ensure to open port 8080 in your AWS security group for both instances.
- Keep `.pem` key files secure and use `chmod 400` before connecting via SSH.
- For Tomcat, be careful editing XML files — use `vi` properly to save changes.
