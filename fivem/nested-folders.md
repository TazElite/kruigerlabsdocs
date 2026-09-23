---
title: "Fixing Double/Nested Resource Folders"
description: "A practical step-by-step Kruiger Labs guide to fixing double/nested resource folders."
category: "FiveM Servers"
order: 94
keywords: "Fixing Double/Nested Resource Folders step by step Kruiger Labs"
---

# Fixing Double/Nested Resource Folders

This guide walks through **Fixing Double/Nested Resource Folders** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## Create the resource

Use a dedicated folder under `resources/[local]` or another category. The resource root needs `fxmanifest.lua`; keep client and server responsibilities separate.

## Manifest starter

```lua
fx_version 'cerulean'
game 'gta5'
author 'YourName'
description 'Resource description'
version '1.0.0'
client_script 'client.lua'
server_script 'server.lua'
```

## Develop in small steps

Start with one observable behavior. Run `refresh` after adding a new resource, `ensure ResourceName` to start it, and `restart ResourceName` after edits. Watch both server console and F8.

## Security boundary

Clients are not authoritative. Validate permissions, amounts, target IDs and state-changing requests server-side. Use local events when networking is unnecessary.

## Release-quality check

Cold boot, reconnect, test two players, test allowed/denied permissions, inspect performance, remove debug spam, document config/dependencies, and tag a version.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
