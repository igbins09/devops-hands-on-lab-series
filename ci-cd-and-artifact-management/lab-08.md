# Lab 08 – Nexus Setup on Red Hat and Integration with Jenkins

**Category:** CI/CD & Artifact Management

---

## Objective

Install and configure Sonatype Nexus on a Red Hat EC2 instance for artifact storage, then integrate it with Jenkins to upload build artifacts.

---

## Tools Used

- Red Hat EC2 instance
- Java 8
- Nexus 3
- Jenkins
- Nexus Artifact Uploader Plugin

---s

## Steps Taken

### Nexus Installation
1. Launched a small Red Hat EC2 instance and opened port 8081 in the security group.
2. Installed Java 8 and downloaded the latest Nexus 3 archive.
3. Extracted Nexus and configured proper permissions under a new `nexus` user.
4. Updated memory settings and configured Nexus to run as a systemd service.
5. Enabled the service and verified it was running via logs and status checks.
6. Accessed Nexus via browser and retrieved the admin password from the instance.
7. Logged in, changed the admin password, and confirmed the dashboard loaded successfully.

### Jenkins Integration
1. Installed the Nexus Artifact Uploader plugin in Jenkins.
2. In an existing Freestyle job:
   - Configured GitHub as the SCM
   - Added Maven build steps (`clean install`)
   - Added a Nexus artifact upload step with appropriate repository and artifact details
3. Ran a build and verified the `.war` artifact was successfully uploaded to the `maven-snapshots` repository in Nexus.

---

## What I Learned

- How to set up and secure a Nexus binary repository on Red Hat Linux.
- How to upload build artifacts to Nexus directly from Jenkins.
- Basics of artifact versioning and repository configuration.
