---
title: "Resource Start Order & Dependencies"
description: "Build a startup order that prevents missing exports, framework failures, and boot-only errors."
category: "FiveM Servers"
order: 55
keywords: "Resource Start Order & Dependencies FiveM step by step"
---

# Resource Start Order & Dependencies
Many “works after restart but not after boot” problems are dependency-order problems.

## Build the chain
For each resource, ask: **what must already be running before this starts?**

Example concept:

```text
database adapter
      ↓
framework/core
      ↓
shared libraries
      ↓
feature resources
      ↓
optional UI/add-ons
```

Do not copy this blindly; use each resource's documentation.

## Test a cold boot
A restart test is not enough. Stop the server completely, start it normally, and verify there are no dependency/export errors.

## Success check
The server boots cleanly from a stopped state without manually restarting resources to make them work.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
