---
title: "FiveM Server Basics"
description: "A beginner-friendly path from a messy resources folder to an organized FiveM server."
category: "FiveM Servers"
order: 10
keywords: "FiveM beginner resources bracket folders ensure resource organization"
---

# FiveM Server Basics

This guide focuses on organization and maintainability. It does **not** require a specific framework.

## Understand the server data folder
A typical FiveM server data directory contains `server.cfg` and a `resources` directory. Resources are folders containing an `fxmanifest.lua` (or older `__resource.lua`) and the files that resource needs.

> **Tip:** Back up your server before reorganizing an existing production server.

## Organize resources with bracket folders
FiveM supports category folders wrapped in square brackets. The brackets are part of the folder name.

```text
resources/
├── [core]/
├── [standalone]/
├── [kruiger]/
├── [maps]/
├── [vehicles]/
├── [eup]/
└── [voice]/
```

A bracket folder is an organizational container. Put complete resource folders **inside** it.

```text
resources/
└── [kruiger]/
    ├── KruigerHandsUp/
    │   ├── fxmanifest.lua
    │   ├── client.lua
    │   └── config.lua
    └── KruigerDV/
        ├── fxmanifest.lua
        └── client.lua
```

Do not put the files from multiple resources directly into `[kruiger]`.

## Start resources
You can start one resource:

```cfg
ensure KruigerHandsUp
```

Or ensure a category:

```cfg
ensure [kruiger]
```

For a new server, explicit `ensure` lines are often easier to troubleshoot because you can see the intended order. Category ensures are useful when a group is independent and intentionally managed together.

## Choose a predictable order
Start dependencies before resources that use them. A clean layout might be:

```cfg
# Core / framework
ensure [core]

# Voice
ensure [voice]

# Standalone resources
ensure [standalone]

# Kruiger Labs
ensure [kruiger]

# Maps and assets
ensure [maps]
ensure [vehicles]
```

Your exact order depends on your resources and framework.

## Keep names stable
Renaming a resource can break exports, dependencies, configuration, or code that refers to the resource by name. Keep the distributed resource name unless its documentation explicitly says renaming is supported.

## Next steps
Continue with **Organizing Resources**, **Cleaning server.cfg**, **Multiple CFG Files**, and **ACE Permissions**.
