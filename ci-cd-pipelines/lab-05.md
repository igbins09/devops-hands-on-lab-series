# Lab 05 – Make Code Changes to Trigger Jenkins Builds Instantly

**Category:** CI/CD Pipelines

---

## Objective

Simulate a real code change to verify that GitHub webhooks successfully trigger Jenkins builds without manual intervention.

---

## Tools Used

- Git Bash / iTerm (from EC2)
- Git (CLI)
- GitHub

---

## Steps Taken

1. Connected to the Jenkins EC2 instance and verified the repo folder was already cloned.
2. Navigated to `MyWebApp/src/main/webapp` and edited `index.jsp`:
   - Replaced the heading with:  
     `<h2>Howdy Folks !!! Welcome to DevOps!</h2>`
3. Staged and committed the change:
   - `git add index.jsp`
   - `git commit -m "made change to jsp"`
   - `git push`
4. Verified the change appeared in the GitHub repo and confirmed Jenkins triggered the build instantly via webhook.

---

## What I Learned

- The Git workflow from code change to commit and push using CLI.
- How to confirm webhook-based automation end-to-end.
- Jenkins builds can be triggered instantly without SCM polling when properly configured.

---

## Notes

- Always use `git pull` before editing to stay synced with remote.
- Use `:wq!` in `vi` to save and exit without confusion.
- Keep commit messages clear and relevant for tracking changes.

