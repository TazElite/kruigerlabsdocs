---
title: "KruigerPriority"
description: "Configure and operate the Kruiger Labs roleplay priority system, including statuses, permissions, cooldown behavior, and troubleshooting."
category: "Paid Scripts"
order: 200
keywords: "KruigerPriority configuration commands ACE permissions troubleshooting"
---

# KruigerPriority

KruigerPriority is the Kruiger Labs standalone priority-management component for roleplay servers. It is built around four operational states:

- **Available** — priority can be started.
- **Active** — a priority is currently in progress.
- **On Hold** — new priorities should not begin.
- **Cooldown** — a completed priority is in its cooldown period.

## Before installation
Back up your server configuration. Remove or disable another priority resource only after you know KruigerPriority is ready to replace it. Two priority systems controlling the same status will produce confusing results.

## Installation
1. Upload the complete KruigerPriority resource folder.
2. Keep the distributed resource name unless your release explicitly supports renaming.
3. Open the editable configuration supplied with your purchased version.
4. Configure the statuses/cooldown and permissions you intend to use.
5. Add the documented ACE rules before the resource starts.
6. Add the resource to `server.cfg`.
7. Cold boot the server and watch the console.
8. Test as both an authorized and unauthorized player.

## Command
The suite/product command established for priority management is:

```text
/priority
```

Use the command interface exposed by your installed version to change the priority state.

## ACE permissions
KruigerPriority uses the `kruiger.priority.*` ACE namespace. Use the exact ACE objects shipped with your installed version for individual actions; do not guess a suffix from an older release.

A clean permission layout belongs before the resource starts:

```cfg
# KruigerPriority permissions
# Add the exact kruiger.priority.* ACEs documented in your release here.

ensure KruigerPriority
```

## Configuration checklist
Before launch verify:
- starting/default state
- allowed priority statuses
- cooldown duration/behavior
- who may start/change/end priority
- display/UI settings exposed by your release
- logging/webhook settings if enabled
- whether any department-specific rules are configured

## Test plan
1. Boot into **Available**.
2. Start a priority with an authorized account.
3. Confirm a non-authorized account cannot administratively change it.
4. Move through **Active → Cooldown → Available**.
5. Test **On Hold**.
6. Reconnect a player and confirm the visible state is synchronized.
7. Restart the resource/server and verify the intended initial/persisted behavior for your version.

## Troubleshooting
### `/priority` is missing
Confirm the resource actually started. Read the first KruigerPriority-related console error.

### Permission denied
Check the exact `kruiger.priority.*` ACE used by the installed version, principal inheritance, and that your ACE file executes before the resource starts.

### Status changes for one player but not others
Look for client errors and conflicting priority resources. Test with only KruigerPriority controlling the priority display.

### Cooldown appears wrong
Check the configured cooldown unit/value and verify an older configuration was not copied over a newer release.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
