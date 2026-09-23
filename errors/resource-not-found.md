---
title: "Couldn't find resource"
description: "FiveM cannot discover the named resource."
category: "Error Encyclopedia"
order: 10
keywords: "Couldn't find resource error fix"
---

# Couldn't find resource

## What it usually means
FiveM cannot discover the named resource.

## Fix it in this order
1. Confirm the folder exists under `resources`.
2. Confirm `fxmanifest.lua` is directly inside the actual resource root.
3. Run `refresh` and read manifest errors.
4. Check the name used by `ensure` exactly matches the resource folder.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
