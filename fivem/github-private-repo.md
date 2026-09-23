---
title: "Private GitHub Deployment"
description: "Connect a FiveM host to a private GitHub repository using narrowly scoped access."
category: "FiveM Servers"
order: 95
keywords: "Private GitHub Deployment FiveM step by step"
---

# Private GitHub Deployment
A private repository is appropriate when your server files should not be public.

## Recommended server access
For a machine that only needs to pull one repository, use repository-scoped read-only deployment access when possible.

## Deploy-key approach
Generate an SSH key on the server:

```bash
ssh-keygen -t ed25519 -C "fivem-deploy"
```

Add the **public** key as a deploy key to the intended repository. Keep the private key on the server.

Clone using the repository's SSH URL, then test:

```bash
git pull origin main
```

## Security
Do not reuse a broad personal token if a narrower read-only credential solves the problem. Never commit the private key.

## Success check
The server can clone/pull the intended private repository but does not have unnecessary access to unrelated repositories.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
