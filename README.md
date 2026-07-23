# Linux+ XK0-006 Milestones

**Student:** Margaret Dunsmore
**Course:** CompTIA Linux+ XK0-006 — FastForward Track
**Year:** 2025–2026

---

## Repository Structure

```
linux-plus-milestones/
├── README.md                    # This file — update with your information
├── Dockerfile                   # Container image definition (provided)
├── run_container.sh             # Container launcher (provided)
├── test_deploy.sh               # Verification script (provided)
├── deploy.sh                    # YOUR M2 deployment script (you write this)
├── design_document.md           # YOUR M2 design decisions (you write this)
└── m1/
    └── hardening_report.docx    # YOUR M1 submission (you upload to Canvas)
```

---

## Milestone 1 — Linux Server Hardening Assessment

**Due:** Before Class 8, 9:00 AM
**Submitted via:** Canvas (upload hardening_report.docx)
**Presented:** Class 8 — 5 minutes

[Brief description of your approach — fill this in after completing M1]

---

## Milestone 2 — Bash Server Deployment Script

**Due:** Before Class 10, 9:00 AM
**Submitted via:** Canvas (submit this repo URL)
**Presented:** Class 10 — 10 minutes (7 min walkthrough + 3 min Q&A)

### What my script does
My script creates a webserver system account and configures the web server directory to only be writable by the webserver system account. It then installs and turns on Apache2, and sets Apache to run automatically on system startup. Then it updates the firewall so that the only open incoming ports are HTTP and HTTPS (80 and 443). Finally it sets up a weekly cron job that runs logrotate.

### Container environment
- Base image: ubuntu:22.04
- Run with: `bash run_container.sh`
- Test with: `bash test_deploy.sh`

### Key decisions I made
[List 2-3 specific decisions you made and why — fill this in before submitting]

### AI Collaboration summary
I used Google Gemini to explain how to set up a weekly cron job for logrotate. I was able to verify this using the container and the test_deploy.sh, and also with CompTIA's explaination of cron jobs. I also used Google Gemini to check my initial scripts for errors - it found one place where I forgot to use sudo and it also made recommendations about how to change things so they work in a docker environment, but I ignored the docker suggestions because this is not meant to be run in a docker environment, even though we used docker for the assignment.

---

## Commit History

[Your commit history will appear here on GitHub automatically]

*At least 3 meaningful commits required. Commit messages should describe what changed.*