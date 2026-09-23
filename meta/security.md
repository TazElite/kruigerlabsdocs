---
title: "Documentation Security Rules"
description: "Rules for safely following examples without exposing production secrets."
category: "Documentation"
order: 3
keywords: "Documentation Security Rules"
---

# Documentation Security Rules
Examples use placeholders intentionally.

Never publish or commit:
- Discord bot tokens
- GitHub/GitLab access tokens
- database passwords/connection strings
- FiveM server/license keys
- private keys
- complete webhook URLs
- customer/private data

If a secret is exposed, deleting the message/file is not enough. Rotate/revoke the credential, replace it everywhere it is used, and inspect access/logs as appropriate.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
