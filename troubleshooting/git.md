---
title: "Git Deployment Troubleshooting"
description: "Fix common clone, pull, authentication, branch, and local-change problems."
category: "Troubleshooting"
order: 410
keywords: "Git troubleshooting clone pull deploy key permission denied local changes"
---

# Git Deployment Troubleshooting

## Authentication failed
For a private repository, verify the server has the intended deploy key/token and that it has access to that repository.

## Permission denied (publickey)
Check that the SSH private key exists on the server, the public key was added to the correct repository/account, and SSH is using the expected key.

## `git pull` refuses because of local changes
Do not blindly force/reset production files. Run:

```bash
git status
git diff
```

Decide whether the server-side changes should be committed, backed up, or discarded.

## Wrong branch
Check:

```bash
git branch --show-current
git remote -v
```

Then pull the branch your deployment actually uses.

## Repository contains a secret
Rotate the secret immediately. Removing it from the newest file does not make previous Git history safe.
