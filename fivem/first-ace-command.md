---
title: "Protecting a Command With ACE"
description: "A practical step-by-step Kruiger Labs guide to protecting a command with ace."
category: "FiveM Servers"
order: 138
keywords: "Protecting a Command With ACE step by step Kruiger Labs"
---

# Protecting a Command With ACE

This guide walks through **Protecting a Command With ACE** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## Mental model

ACE is FiveM's permission system. An ACE grants or denies a named capability to a principal. Principals can inherit from groups, so design groups first instead of copying permissions onto every player.

## Basic pattern

```cfg
add_ace group.admin command allow
add_ace group.admin command.quit deny
add_principal identifier.fivem:YOUR_ID group.admin
```
Use real identifiers only in your private server configuration.

## Split permissions cleanly

Keep larger permission sets in `permissions.cfg`, then load them from `server.cfg` with:
```cfg
exec permissions.cfg
```
Place resource-specific ACEs before the resource starts when that resource reads permissions during initialization.

## Test correctly

Test once as an authorized user and once as a normal user. If both succeed, your permission is probably too broad; if both fail, inspect the exact ACE object and principal inheritance.

## Debug checklist

Confirm spelling/case, the actual player identifier, file execution order, inherited groups, explicit denies, and the exact permission object expected by the resource.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
