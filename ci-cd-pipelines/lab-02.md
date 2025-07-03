# Lab 02 – Create Java Web App Using Maven & Push to GitHub

**Category:** CI/CD Pipelines

---

## Objective

Create a Java web application using Maven and push the project into a private GitHub repository using SSH authentication from the Jenkins EC2 instance.

---

## Tools Used

- GitHub
- Git CLI
- SSH keys
- Maven
- EC2 (Ubuntu)

---

## Steps Taken

1. **Created a private repository on GitHub** and initialized it with a README.
2. **Generated SSH keys** on the Jenkins EC2 instance using `ssh-keygen`, then copied the public key to GitHub under SSH settings.
3. **Cloned the repository** using the SSH URL to the EC2 instance.
4. **Generated a new Java Web App** using Maven’s `archetype:generate` command with group and artifact IDs.
5. **Configured Git user details** locally on the EC2 instance.
6. **Staged and committed the project files** using `git add` and `git commit`.
7. **Pushed the Java Web App** to the GitHub remote repository via SSH.
8. **Verified the commit** and project structure on GitHub.

---

## What I Learned

- How to securely connect to GitHub from a remote Linux server using SSH keys.
- How to use Maven to scaffold a Java web application.
- The full Git workflow: clone, add, commit, and push — all from the terminal.

---

## Notes

- Avoid regenerating SSH keys if one already exists; reuse when possible.
- Ensure GitHub is configured for SSH (not HTTPS) when cloning the repo.
- After running Maven, check `git status` to confirm files are properly tracked before pushing.

