---
title: "Planning Your FiveM Server"
description: "Plan the framework, resources, hosting, database, permissions, and deployment before installing scripts."
category: "FiveM Servers"
order: 15
keywords: "Planning Your FiveM Server FiveM step by step"
---

# Planning Your FiveM Server
A reliable server starts with a plan instead of a pile of resources.

## Step 1 — Decide what you are building
Write down the server type, expected player count, framework (if any), database needs, voice system, administration system, and the features required for launch.

## Step 2 — Separate required from optional
Create three lists: **required for boot**, **required for launch**, and **nice later**. Install the smallest working server first.

## Step 3 — Choose a folder standard
Use bracket categories consistently. Example:

```text
resources/
├── [core]/
├── [framework]/
├── [standalone]/
├── [kruiger]/
├── [voice]/
├── [maps]/
├── [vehicles]/
└── [eup]/
```

## Step 4 — Track dependencies
For every resource, record what it requires and what requires it. Dependencies must be installed and normally started first.

## Step 5 — Plan backups
Keep at least one known-good copy of configuration and important data away from the live server.

## Step 6 — Build in stages
Boot → framework/database → one feature group → test → next group. This makes the last change obvious when something breaks.

## Success check
Before continuing, you should know where every resource belongs, which resources are dependencies, where your secrets live, and how you will restore a working backup.
