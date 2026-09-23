---
title: "KruigerNPC"
description: "ACE-controlled standalone NPC and traffic toggle."
category: "Free Scripts"
order: 130
keywords: "KruigerNPC FiveM free script install configuration troubleshooting"
---

# KruigerNPC

A standalone NPC/traffic control resource intended for authorized staff use.

## Installation

```cfg
ensure KruigerNPC
```

## Usage
The resource provides `/togglenpc` for authorized users. It can disable/restore configured ambient NPC and traffic behavior.

## Permissions
KruigerNPC is designed around ACE authorization. Use the exact ACE object included with your downloaded release; do not invent an ACE name from an older guide.

Keep ACE entries in a central `permissions.cfg` if that matches your server organization.

## Troubleshooting
If `/togglenpc` exists but access is denied, verify the ACE object, principal/group membership, and that `permissions.cfg` executes before testing. If traffic returns unexpectedly, check for other population/traffic resources.
