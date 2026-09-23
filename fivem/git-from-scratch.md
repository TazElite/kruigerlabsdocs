---
title: "Git From Scratch"
description: "A beginner step-by-step Git workflow for versioning FiveM configuration and resources you are allowed to store."
category: "FiveM Servers"
order: 85
keywords: "Git From Scratch FiveM step by step"
---

# Git From Scratch
Git tracks changes. GitHub and GitLab can host the remote repository.

## Before you begin
Only store files you own or are licensed to place in the repository. Never commit secrets.

## Basic workflow
Clone:

```bash
git clone YOUR_REPOSITORY_URL
cd YOUR_REPOSITORY
```

Inspect:

```bash
git status
```

Update from the remote:

```bash
git pull origin main
```

For changes you intentionally maintain:

```bash
git add .
git commit -m "Update server configuration"
git push origin main
```

## Production rule
Do not use `git add .` blindly until you understand what is untracked. Run `git status` first.

## Success check
You can clone a fresh copy, pull an update, see what changed, and restore the previous known-good version.
