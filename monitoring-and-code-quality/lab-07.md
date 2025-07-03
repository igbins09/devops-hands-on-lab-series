# Lab 07 – Enable Scanning for PL/SQL Files in SonarQube

**Category:** Monitoring & Code Quality

---

## Objective

Enable support for scanning PL/SQL files in SonarQube by installing an open-source community plugin.

---

## Tools Used

- SonarQube
- sonar-plsql open plugin

---

## Steps Taken

1. Navigated to the SonarQube extensions directory:  
   `cd /opt/sonarqube/lib/extensions`
2. Downloaded the PL/SQL plugin JAR:  
   `wget https://github.com/felipebz/sonar-plsql/releases/download/2.0.0/sonar-plsql-open-plugin-2.0.0.jar`
3. Restarted the SonarQube service:  
   `sudo systemctl stop sonar` → `sudo systemctl start sonar`
4. Checked service status and confirmed that SonarQube was running.
5. Logged into SonarQube UI and confirmed that PL/SQL rules appeared under Quality Profiles.

---

## What I Learned

- How to install and manage third-party plugins in SonarQube.
- How to restart services safely and validate plugin registration.
- Where to check SonarQube logs for troubleshooting (`web.log`).

---

## Notes

- If SonarQube fails to start, review logs at `/opt/sonarqube/logs/` for error messages.
- PL/SQL support helps expand code quality tracking to legacy and database layers.

