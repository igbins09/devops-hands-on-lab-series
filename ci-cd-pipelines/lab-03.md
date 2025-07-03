# Lab 03 – Automate Build and Deployment of Java WebApp Using Jenkins

**Category:** CI/CD Pipelines

---

## Objective

Configure Jenkins to automatically build and deploy a Java web application from GitHub to a Tomcat server.

---

## Tools Used

- Jenkins
- GitHub (SCM)
- Maven
- Tomcat 9
- JaCoCo (Code Coverage)
- Deploy to Container Plugin

---

## Steps Taken

1. **Created a new freestyle Jenkins job** named `myFirstAutomateJob`.
2. **Connected the job to GitHub** by providing the repository SSH URL and adding credentials via a GitHub personal access token.
3. **Configured Jenkins to poll SCM** every 2 minutes (`H/02 * * * *`) for code changes.
4. **Set up Maven build step** using `clean install` and specified the path to the `pom.xml` file inside the `MyWebApp` folder.
5. **Installed required plugins**: “Deploy to Container” and “JaCoCo” for code coverage tracking.
6. **Configured post-build steps**:
   - Recorded code coverage using JaCoCo.
   - Deployed the generated WAR file (`**/*.war`) to Tomcat 9 using provided credentials and public DNS.
7. **Triggered the build** and verified deployment by accessing the app through Tomcat at:  
   `http://<public_dns>:8080/MyWebApp`

---

## What I Learned

- How to integrate Jenkins with GitHub using personal access tokens (PAT).
- How to automate Java build and deployment using Maven and Jenkins.
- How to deploy a WAR file to Tomcat from a Jenkins pipeline.
- How to monitor build output and troubleshoot errors using Jenkins console logs.

---

## Notes

- Ensure Maven is configured under “Global Tool Configuration” in Jenkins.
- Verify WAR deployment path and public DNS carefully during testing.

