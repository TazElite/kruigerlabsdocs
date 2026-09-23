---
title: "Cleaning server.cfg"
description: "Keep startup settings readable without turning server.cfg into an unmanageable wall of configuration."
category: "FiveM Servers"
order: 30
keywords: "server.cfg organize clean exec secrets gitignore FiveM"
---

# Cleaning server.cfg

`server.cfg` should remain the main entry point for your server. It can stay readable even on a large server.

## Keep important server settings visible
Settings that define the server itself, startup order, endpoints, and major behavior can remain in `server.cfg`.

Use comments to create clear sections:

```cfg
# ============================================================
# SERVER
# ============================================================

# ============================================================
# CONFIG FILES
# ============================================================

# ============================================================
# RESOURCES
# ============================================================
```

## Move large logical groups
If hundreds of ACE entries or a large product configuration makes `server.cfg` difficult to read, move that logical group to another CFG and load it with `exec`.

```cfg
exec permissions.cfg
exec voice.cfg
```

Do not split files merely to create more files. A separate CFG is useful when it gives a large, clearly defined configuration one home.

## Keep secrets out of public repositories
License keys, database passwords, bot tokens, API keys, webhooks, and other credentials should not be committed to a public repository.

If you use Git to manage server configuration, keep sensitive values in a server-only file that is ignored by Git, or use your host's secret/environment features when supported.

```gitignore
secrets.cfg
*.log
cache/
```

If a secret is accidentally committed, removing it in a later commit does not make the old secret safe. Rotate the exposed credential.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
