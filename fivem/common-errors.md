---
title: "Common FiveM Errors"
description: "Recognize missing manifests, dependency errors, missing exports, configuration mistakes, and permission failures."
category: "FiveM Servers"
order: 165
keywords: "Common FiveM Errors FiveM step by step"
---

# Common FiveM Errors

## Resource manifest missing
Verify `fxmanifest.lua` exists directly inside the resource folder.

## Couldn't find dependency
Install/start the documented dependency first and verify the resource name is exact.

## No such export
Usually indicates the providing resource is missing, failed, outdated, renamed, or started too late.

## Unknown command
Confirm the resource registered the command and started successfully.

## Permission denied
Verify the exact ACE, group/principal mapping, and configuration load order.

## Works only after manual restart
Investigate dependency/start order.

## Database connection error
Verify host, port, database, username, password, network access, and database service status without posting credentials publicly.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
