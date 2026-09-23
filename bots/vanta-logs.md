---
title: "Vanta Logging"
description: "Configure Vanta's logging categories, invite logs, event routing, and common logging problems."
category: "Bots"
order: 325
keywords: "Vanta Logging Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Logging
Start logging configuration with:

```text
/setup logs
```

Invite-specific logging is available through:

```text
/invites logs
```

## Established logging areas
Vanta's advanced logging work covers **Messages, Members, Moderation, Channels, Roles, Invites, Server Events, and server/level/boost events**.

## Invite attribution
When Vanta cannot reliably determine which invite caused a join, it should report the attribution as unknown rather than guessing.

## Good practice
Use separate channels when one channel becomes noisy. Give log channels staff-only visibility where the contents are sensitive.

## Troubleshooting
If one category is missing while others work, check that category's configured destination and Vanta's channel permissions before rebuilding the entire logging setup.
