# Lab 06 – Set Up SonarQube and Integrate with Jenkins

**Category:** Monitoring & Code Quality

---

## Objective

Install SonarQube 8 on a new Ubuntu EC2 instance and integrate it with Jenkins to enable static code analysis during Java build pipelines.

---

## Tools Used

- Ubuntu EC2 (minimum 2GB RAM)
- SonarQube 8.6
- PostgreSQL
- Jenkins
- Maven
- SonarQube Jenkins Plugin

---

## Steps Taken

### SonarQube Installation
1. Installed Java 11, PostgreSQL, and created a database user for SonarQube.
2. Downloaded and extracted SonarQube into `/opt/sonarqube`.
3. Created a dedicated `sonar` user and group with proper permissions.
4. Configured the `sonar.properties` file with database credentials and JDBC URL.
5. Set `RUN_AS_USER=sonar` in the SonarQube startup script.
6. Created a systemd service file to manage SonarQube as a service.
7. Adjusted system kernel settings and limits for performance and compatibility.
8. Started and enabled the SonarQube service and verified logs for successful startup.
9. Accessed the SonarQube UI using the public DNS on port 9000.

### Jenkins Integration
1. Logged into SonarQube, generated a global token.
2. In Jenkins, configured SonarQube under "Configure System" using the token and server URL.
3. Edited an existing freestyle Jenkins job:
   - Enabled “Prepare SonarQube Scanner Environment”
   - Set Maven goal as `clean install sonar:sonar`
4. Triggered a Jenkins build and confirmed that code analysis results appeared in SonarQube.

---

## What I Learned

- Full setup and configuration of SonarQube on Linux including database and permissions.
- How to integrate SonarQube with Jenkins and use it in a Maven pipeline.
- Where to troubleshoot SonarQube issues using logs and system settings.

---

## Notes

- Ensure EC2 instance has at least 2GB RAM for SonarQube to start properly.
- Port 9000 must be opened in the AWS security group.
- Use the global token from SonarQube instead of username/password in Jenkins integration.

