---
title: "Private GitLab Deployment"
description: "Use GitLab deploy keys and a controlled pull workflow for FiveM servers."
category: "FiveM Servers"
order: 105
keywords: "Private GitLab Deployment FiveM step by step"
---

# Private GitLab Deployment
GitLab can be used the same way as GitHub for a Git-backed FiveM workflow.

## Flow
1. Create/import your repository.
2. Create an SSH deploy key on the FiveM host.
3. Add the public key to the project with the minimum required access.
4. Clone over SSH.
5. Test a pull.
6. Keep production deployment controlled.

## Do not mix live edits and Git carelessly
If you edit tracked files directly on the server, a later pull can conflict. Prefer editing in your normal development copy, committing, then pulling the reviewed commit to production.

## Success check
`git status` is clean after deployment and the server can pull the intended branch without interactive account credentials.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
