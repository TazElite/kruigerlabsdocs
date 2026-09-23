---
title: "Vanta Server Backups"
description: "Create, list and restore Vanta guild backups using the non-destructive restore workflow."
category: "Bots"
order: 335
keywords: "Vanta Server Backups Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Server Backups
Backups are under `/guild`:

```text
/guild backup-create
/guild backup-list
/guild backup-restore
```

Backup restore requires **Administrator** in the established workflow.

## Non-destructive restore
Vanta's restore design recreates missing items without deleting or overwriting existing roles/channels. This is intentionally safer than treating restore as “erase the server and replace everything.”

## Before restore
Review what exists, use an administrator account, and understand that a backup is not a replacement for every Discord/server data backup need.
