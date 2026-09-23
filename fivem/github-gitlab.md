---
title: "GitHub & GitLab for FiveM Servers"
description: "Use Git safely to organize and deploy server files without exposing credentials."
category: "FiveM Servers"
order: 70
keywords: "GitHub GitLab FiveM git clone pull deploy key private repository secrets"
---

# GitHub & GitLab for FiveM Servers

Git can make server updates repeatable and give you history when a configuration change goes wrong.

## What Git should manage
Good candidates:
- configuration templates without secrets
- scripts you own or are licensed to store
- documentation
- custom resources you control

Do **not** upload paid third-party resources to a repository unless your license allows it.

## Start with an existing remote repository

```bash
git clone YOUR_REPOSITORY_URL
cd YOUR_REPOSITORY
```

After changes are committed upstream:

```bash
git pull origin main
```

## Public vs private
Use a private repository for server code/configuration that should not be public. A private repository still requires careful secret handling: collaborators and automation with access can read repository history.

## Deploy keys
For a server that only needs to download updates, a repository-scoped **read-only deploy key** is preferable to giving the server broad account access.

Typical SSH key creation:

```bash
ssh-keygen -t ed25519 -C "fivem-deploy"
```

Add the **public** key to the repository's deploy-key settings. Keep the private key on the server and protect its file permissions.

## Do not blindly auto-deploy production
A safer workflow is:

```text
Edit → Commit → Review → Pull to server → Restart affected resource → Test
```

Automatic deployment can be useful, but a broken commit can become a broken live server immediately.

## GitHub and GitLab
Both can host the repository. The basic Git workflow is the same. Their web interfaces use different names/locations for some deployment and access-control features.

## Secrets
Never commit:
- FiveM license keys
- database passwords
- Discord bot tokens
- webhook tokens
- API keys
- private keys

If one is committed, rotate it.
