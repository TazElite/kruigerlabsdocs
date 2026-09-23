---
title: "Discord bot cannot assign/manage role"
description: "Discord hierarchy or permissions block the bot."
category: "Error Encyclopedia"
order: 21
keywords: "Discord bot cannot assign/manage role error fix"
---

# Discord bot cannot assign/manage role

## What it usually means
Discord hierarchy or permissions block the bot.

## Fix it in this order
1. Give the bot Manage Roles only when needed.
2. Move the bot role above the role it must manage.
3. Confirm the target role is not managed by another integration.
4. Test with a normal member.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
