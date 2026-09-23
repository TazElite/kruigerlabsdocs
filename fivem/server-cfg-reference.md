---
title: "server.cfg Explained"
description: "A section-by-section guide to keeping the main FiveM configuration readable and maintainable."
category: "FiveM Servers"
order: 45
keywords: "server.cfg Explained FiveM step by step"
---

# server.cfg Explained
`server.cfg` is the main configuration entry point for a typical FiveM server.

## Keep it readable
Use headings and comments:

```cfg
# ============================================================
# NETWORK / SERVER
# ============================================================

# ============================================================
# EXTERNAL CONFIGURATION
# ============================================================
exec permissions.cfg

# ============================================================
# RESOURCES
# ============================================================
ensure [core]
ensure [standalone]
ensure [kruiger]
```

This is an organizational example, not a universal startup order.

## What `ensure` does
`ensure ResourceName` starts a stopped resource and restarts it if already running. FiveM also supports category names.

## What `exec` does
`exec filename.cfg` runs commands from another file relative to the server data directory. Use it for a large logical configuration group.

## Keep credentials private
Do not publish license keys, database passwords, bot tokens, API keys, webhooks, or private keys.

## Success check
A new administrator should be able to open your main CFG and quickly find server settings, external CFGs, and resource startup order.
