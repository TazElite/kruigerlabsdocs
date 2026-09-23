---
title: "Production Maintenance Checklist"
description: "A repeatable pre-change, deployment, restart, and post-change checklist for live FiveM servers."
category: "FiveM Servers"
order: 155
keywords: "Production Maintenance Checklist FiveM step by step"
---

# Production Maintenance Checklist
Use the same process every time you touch production.

## Before
- Read changelogs.
- Back up affected files/data.
- Check dependencies and migrations.
- Tell staff/players if downtime is expected.
- Know your rollback.

## Deploy
- Make one logical change.
- Watch the console from the beginning of startup.
- Do not ignore the first relevant error.

## Verify
- Connect as a normal player.
- Test the changed feature.
- Test permissions.
- Test persistence when relevant.
- Test a cold boot for dependency changes.

## After
- Record what changed.
- Keep the known-good rollback until the change has been stable.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
