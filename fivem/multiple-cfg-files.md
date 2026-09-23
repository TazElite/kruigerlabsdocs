---
title: "Using Multiple CFG Files"
description: "Split large FiveM configuration into logical files using exec without making the server harder to understand."
category: "FiveM Servers"
order: 40
keywords: "FiveM exec cfg multiple config permissions.cfg voice.cfg"
---

# Using Multiple CFG Files

FiveM's `exec` command lets one configuration file execute another configuration file.

## Simple structure

```text
server-data/
├── server.cfg
├── permissions.cfg
├── voice.cfg
└── resources/
```

Then load them from `server.cfg`:

```cfg
exec permissions.cfg
exec voice.cfg
```

## What belongs in another CFG?
A good candidate is a large block that has one purpose:
- ACE/principal permissions
- voice configuration
- a resource with a very large set of convars
- a server-only secrets file that is excluded from Git

Normal `ensure` lines can stay in `server.cfg` if that is easier for you to follow.

## Permissions example

`server.cfg`:

```cfg
exec permissions.cfg

ensure KruigerHandsUp
ensure KruigerDV
```

`permissions.cfg`:

```cfg
# Administrators
add_ace group.admin command allow
add_ace group.admin command.quit deny
```

The exact ACE names for a resource must come from that resource's documentation.

## Troubleshooting
If moving a setting breaks something:
1. Confirm the filename is correct.
2. Confirm the file is in the path expected by `exec`.
3. Check the console for an execution error.
4. Check that the CFG is loaded **before** a resource that requires the value at startup.
5. Temporarily move the setting back to `server.cfg` to isolate whether the problem is file loading or the setting itself.
