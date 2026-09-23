---
title: "attempt to index a nil value"
description: "Lua code tried to access a field/value that does not exist at that moment."
category: "Error Encyclopedia"
order: 12
keywords: "attempt to index a nil value error fix"
---

# attempt to index a nil value

## What it usually means
Lua code tried to access a field/value that does not exist at that moment.

## Fix it in this order
1. Use the stack trace to find the first line in your resource.
2. Inspect which variable is nil rather than adding random waits.
3. Validate config/table keys and dependency return values.
4. Add a deliberate guard only when nil is a legitimate state.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
