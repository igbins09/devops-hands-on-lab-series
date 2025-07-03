# Lab 04 – Configure GitHub Webhooks to Trigger Jenkins Builds

**Category:** CI/CD Pipelines

---

## Objective

Configure GitHub webhooks to automatically trigger Jenkins jobs on every code push, enabling instant CI builds without polling.

---

## Tools Used

- GitHub (Webhooks)
- Jenkins (Freestyle Job)
- GitHub Integration Plugin

---

## Steps Taken

1. Enabled the **"GitHub hook trigger for GitScm polling"** in the Jenkins job's Build Triggers section.
2. In the GitHub repository:
   - Navigated to **Settings > Webhooks**
   - Clicked **"Add webhook"**
   - Entered the Jenkins public URL with `/github-webhook/` appended (e.g., `http://<jenkins-dns>:8080/github-webhook/`)
   - Chose **"Just the push event"** and activated the webhook
3. Verified webhook setup by triggering a test event and confirming a **200 OK** response in **Recent Deliveries**.
4. Made a code change in GitHub and confirmed that Jenkins triggered the job instantly.

---

## What I Learned

- How to link GitHub and Jenkins using webhooks instead of polling.
- How to verify webhook delivery and debug using GitHub's webhook settings.
- The value of near-instant CI feedback for developers.

---

## Notes

- Always confirm webhook delivery status to catch misconfigurations early.

