---
title: "Lua/JS syntax error"
description: "The runtime cannot parse the script."
category: "Error Encyclopedia"
order: 13
keywords: "Lua/JS syntax error error fix"
---

# Lua/JS syntax error

## What it usually means
The runtime cannot parse the script.

## Fix it in this order
1. Read the exact file and line/column.
2. Inspect nearby commas, quotes, brackets, `end` statements or braces.
3. Undo the most recent edit if necessary.
4. Restart only after the file parses cleanly.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
