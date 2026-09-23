---
title: "ACE Principals & Groups"
description: "A practical step-by-step Kruiger Labs guide to ace principals & groups."
category: "FiveM Servers"
order: 87
keywords: "ACE Principals & Groups step by step Kruiger Labs"
---

# ACE Principals & Groups

This guide walks through **ACE Principals & Groups** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

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
