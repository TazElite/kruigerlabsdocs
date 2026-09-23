---
title: "KruigerPriority"
description: "Priority status management for roleplay servers."
category: "Paid Scripts"
order: 200
keywords: "KruigerPriority paid FiveM install setup troubleshooting"
---

# KruigerPriority

KruigerPriority provides a dedicated priority-status system for roleplay servers.

## Installation
1. Download the package from your authorized Kruiger Labs delivery/store access.
2. Extract the complete resource into your server resources directory.
3. Read the version-specific README/config included with the package.
4. Add the resource to your startup order.
5. Configure departments/permissions/status behavior exposed by your purchased version.
6. Test every status transition before production.

## Configuration strategy
Keep priority configuration together and document who is allowed to change priority states. If your version uses ACE permissions, place those ACE entries in your server's permission configuration.

## Troubleshooting
If a status does not update, verify the resource is running, the user has the required permission, and no older priority resource is also controlling the same UI/state. Check both client and server console output.
