# Lab 10 – Trigger Jenkins Jobs Directly from Slack

**Category:** DevOps Collaboration

---

## Objective

Enable triggering of Jenkins jobs from Slack using Slack’s Slash Commands feature.

---

## Tools Used

- Slack Slash Commands
- Jenkins
- Slack App Directory

---

## Steps Taken

### Jenkins Configuration
1. Enabled job triggering via token in the Jenkins job configuration.
2. Allowed anonymous read-only access in Jenkins security settings to permit remote job triggering.

### Slack Configuration
1. Created a new Slash Command in the Slack channel (e.g., `/build`).
2. Pointed the command to the Jenkins job URL using the format:  
   `http://<jenkins-dns>/job/<job-name>/build?token=<myToken>`
3. Saved the integration and tested by typing `/build` in the Slack channel.
4. Verified that Jenkins triggered the build successfully.

---

## What I Learned

- How to trigger Jenkins jobs remotely using HTTP requests.
- How Slack can act as a CI/CD trigger mechanism beyond notifications.
- The power of chat-driven DevOps automation in agile environments.
