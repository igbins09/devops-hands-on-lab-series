# Lab 09 – Integrate Slack with Jenkins for Build Notifications

**Category:** DevOps Collaboration

---

## Objective

Connect Jenkins to Slack to send build notifications to a Slack channel using Slack Notifier.

---

## Tools Used

- Slack
- Jenkins
- Slack Notification Plugin

---

## Steps Taken

1. Created a Slack workspace and a dedicated channel.
2. Added the **Jenkins CI** app via Slack integrations and selected the target channel.
3. In Jenkins:
   - Installed the Slack Notifier plugin
   - Configured Slack settings under "Global Slack Notifier Configuration" with workspace, token, and channel
   - Saved token securely using Jenkins credentials (Secret Text)
4. Edited a Jenkins job and added a post-build action to send Slack notifications.
5. Ran a build and confirmed messages appeared in the Slack channel.

---

## What I Learned

- How to integrate third-party communication tools with CI pipelines.
- How to securely manage Slack tokens in Jenkins.
- How build feedback can improve developer awareness and collaboration.
