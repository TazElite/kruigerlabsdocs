---
title: "Free Script Permissions Basics"
description: "A practical step-by-step Kruiger Labs guide to free script permissions basics."
category: "Free Scripts"
order: 409
keywords: "Free Script Permissions Basics step by step Kruiger Labs"
---

# Free Script Permissions Basics

This guide walks through **Free Script Permissions Basics** from preparation through verification, with a rollback path and the checks that matter in a real free scripts environment.

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
