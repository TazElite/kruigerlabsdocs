---
title: "Duplicate chat/HUD/UI"
description: "Two resources are providing overlapping functionality."
category: "Error Encyclopedia"
order: 20
keywords: "Duplicate chat/HUD/UI error fix"
---

# Duplicate chat/HUD/UI

## What it usually means
Two resources are providing overlapping functionality.

## Fix it in this order
1. Identify both implementations.
2. Back up configs.
3. Disable only the replaced component according to its documentation.
4. Cold boot and verify no dependent resource expected the old component.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
