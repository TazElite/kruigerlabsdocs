---
title: "Backups & Rollbacks"
description: "Create a recovery plan before an update, migration, database import, or large configuration change."
category: "FiveM Servers"
order: 115
keywords: "Backups & Rollbacks FiveM step by step"
---

# Backups & Rollbacks
A backup is only useful if you know how to restore it.

## Back up before
- framework updates
- large resource updates
- SQL imports/migrations
- permission rewrites
- mass resource moves
- automated deployment changes

## Keep a known-good version
Label backups with a date and purpose. Do not keep the only backup inside the same live folder you are about to replace.

## Rollback test
For important servers, periodically verify that a backup can actually be restored.

## Success check
You can answer: “If this update breaks the server, exactly which files/data do I restore and how long will it take?”
