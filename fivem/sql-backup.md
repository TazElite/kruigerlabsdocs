---
title: "Backing Up a Database"
description: "A practical step-by-step Kruiger Labs guide to backing up a database."
category: "FiveM Servers"
order: 78
keywords: "Backing Up a Database step by step Kruiger Labs"
---

# Backing Up a Database

This guide walks through **Backing Up a Database** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## Plan the database

Know which database engine/version the resource supports. Create a dedicated database/user where possible, use a strong unique password, and restrict network exposure to what the application actually needs.

## Connection configuration

Keep the connection string server-side. Never place it in client/shared Lua, NUI JavaScript, screenshots, public GitHub, or support posts. Verify hostname, port, database, username and TLS requirements.

## Schema/imports

Back up first. Read SQL migrations before running them. Import only the schema/data required by your installed resource version and do not repeatedly import a destructive migration.

## Test

Start the database adapter before resources that depend on it. Watch for authentication, DNS, timeout, missing-table and duplicate-column errors. Then perform an actual create/read/update path in-game.

## Backup and rollback

Take a database dump before upgrades. A file rollback is not enough when an update also changed schema; document which code version matches which schema.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
