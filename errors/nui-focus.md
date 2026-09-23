---
title: "NUI stuck / cannot move"
description: "Browser focus was enabled but not released."
category: "Error Encyclopedia"
order: 18
keywords: "NUI stuck / cannot move error fix"
---

# NUI stuck / cannot move

## What it usually means
Browser focus was enabled but not released.

## Fix it in this order
1. Use the resource's documented close action.
2. Inspect the close callback and focus-reset code.
3. Restart the affected resource during development if necessary.
4. Ensure every open path has a reliable close/error path.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
