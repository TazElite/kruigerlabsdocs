---
title: "NUI is blank or invisible"
description: "The UI resource runs but its browser interface does not render correctly."
category: "Error Encyclopedia"
order: 17
keywords: "NUI is blank or invisible error fix"
---

# NUI is blank or invisible

## What it usually means
The UI resource runs but its browser interface does not render correctly.

## Fix it in this order
1. Check `ui_page` and manifest `files`.
2. Open client/NUI errors and fix the first browser error.
3. Verify case-sensitive paths and built assets.
4. Check focus/display messages from the client script.

## Prove the fix
Repeat the exact action that originally failed, then perform the relevant restart/reconnect or cold boot. Check logs again even if the visible symptom is gone.

## Escalate
If it still fails, include the exact error, versions, reproduction steps and sanitized configuration in your support report.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
