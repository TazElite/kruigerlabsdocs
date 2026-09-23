---
title: "Installing a FiveM Resource"
description: "A repeatable installation checklist for standalone and framework resources."
category: "FiveM Servers"
order: 60
keywords: "install FiveM resource fxmanifest ensure dependencies"
---

# Installing a FiveM Resource

## 1. Read the resource documentation
Before copying files, check:
- required framework
- dependencies
- SQL files
- configuration files
- ACE permissions
- required start order

## 2. Extract the resource
Do not run a resource from inside a ZIP.

Place the complete folder in a suitable category:

```text
resources/[kruiger]/KruigerHandsUp/
```

Verify:

```text
KruigerHandsUp/
├── fxmanifest.lua
├── client.lua
└── config.lua
```

## 3. Configure it
Open the documented configuration file and change only settings you understand. Keep a backup before large changes.

## 4. Add dependencies first
If a resource depends on another resource, ensure the dependency starts first.

## 5. Ensure the resource

```cfg
ensure KruigerHandsUp
```

## 6. Watch the console
A resource showing `started` is not proof that every feature works. Look for missing dependencies, syntax errors, database errors, and permission errors.

## 7. Test in-game
Test commands, permissions, reconnect behavior, restart behavior, and the feature with more than one player when relevant.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
