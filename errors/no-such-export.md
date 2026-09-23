---
title: "No such export"
description: "A resource is calling an export that is unavailable."
category: "Error Encyclopedia"
order: 11
keywords: "No such export error fix"
---

# No such export

## What it usually means
A resource is calling an export that is unavailable.

## Fix it in this order
1. Confirm the provider resource is installed and started first.
2. Verify the export name and resource name against the installed version.
3. Check whether an update renamed/removed the export.
4. Cold boot after correcting dependency order.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
