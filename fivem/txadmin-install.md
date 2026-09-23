---
title: "Opening txAdmin for the First Time"
description: "A practical step-by-step Kruiger Labs guide to opening txadmin for the first time."
category: "FiveM Servers"
order: 31
keywords: "Opening txAdmin for the First Time step by step Kruiger Labs"
---

# Opening txAdmin for the First Time

This guide walks through **Opening txAdmin for the First Time** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## Preparation

Use the current recommended FXServer artifact and keep server binaries separate from server data. txAdmin is bundled with FXServer; you do not need to install it as a separate resource.

## Initial setup

Run FXServer, open/link txAdmin, authenticate with Cfx, create the server profile, select the appropriate recipe, supply the server registration key, deploy, then save and run.

## Configuration discipline

Keep `server.cfg` readable. Put related settings into clearly labeled sections or `exec` files. Never publish license keys, database credentials, webhooks or API secrets.

## Operational test

Perform a full stop/start, connect from FiveM, verify txAdmin access, inspect the console, and test the server from a normal player's perspective.

## Maintenance

Back up `server-data`, important `txData`/profile data and databases before major changes. Change one layer at a time: artifact, framework, then resources.
