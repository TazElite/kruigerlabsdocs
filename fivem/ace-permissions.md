---
title: "ACE Permissions"
description: "Understand ACE objects, principals, groups, and a maintainable permissions.cfg layout."
category: "FiveM Servers"
order: 50
keywords: "FiveM ACE add_ace add_principal permissions groups"
---

# ACE Permissions

ACE permissions let resources and server commands ask whether a principal has permission to perform an action.

## Core ideas
- **ACE** — a permission rule such as allowing an object.
- **Principal** — the identity or group receiving permissions.
- **Group** — a principal you can use to organize users.
- **Inheritance** — principals can be added to other principals.

Example:

```cfg
add_ace group.admin command allow
add_ace group.admin command.quit deny
```

A resource may define its own ACE object. Always use the exact object documented by that resource.

## Keep permissions together
For larger servers, a dedicated `permissions.cfg` makes auditing easier:

```cfg
# ============================================================
# ADMINISTRATION
# ============================================================

# ============================================================
# KRUIGER LABS
# ============================================================

# ============================================================
# OTHER RESOURCES
# ============================================================
```

Load it early:

```cfg
exec permissions.cfg
```

## Troubleshooting permission denied
Check:
1. The player identifier/principal is correct.
2. The principal was added to the intended group.
3. The resource checks the same ACE object you configured.
4. The permission file actually executed.
5. There is no explicit deny that overrides the behavior you expected.
6. You restarted/reloaded what the resource documentation requires.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
