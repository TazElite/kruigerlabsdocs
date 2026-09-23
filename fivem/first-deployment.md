---
title: "First FiveM Deployment"
description: "From a fresh host to a clean first boot, with checkpoints before you install a framework or custom resources."
category: "FiveM Servers"
order: 5
keywords: "FiveM first deployment host txAdmin Cfx step by step"
---

# First FiveM Deployment

This is the start-to-finish path for a new server owner.

## 1 — Get a host or prepare your machine
If you want managed FiveM hosting, see **Recommended FiveM Hosting**. For self-hosting, follow the current official Cfx server setup for your operating system.

## 2 — Create your Cfx account and server registration
Follow the official Cfx/txAdmin setup and create the required server registration/license key. Treat the key as a credential and do not post it publicly.

## 3 — Get the base server running
Before adding frameworks, maps, vehicles, or paid scripts, make sure the base server boots and you can connect.

## 4 — Back up the clean baseline
This gives you a known-good point before customization.

## 5 — Plan categories
Create only the bracket folders you need.

```text
resources/
├── [core]/
├── [standalone]/
├── [kruiger]/
├── [maps]/
└── [vehicles]/
```

## 6 — Add one system at a time
Install a framework/database if required, test, then add features in small batches.

## 7 — Organize configuration
Keep the main `server.cfg` readable. Move large logical permission/config blocks to separate CFGs only when doing so improves clarity.

## 8 — Secure administration
Use unique credentials, MFA, minimum permissions, private deployment access, and backups.

## 9 — Cold-boot test
Stop the server completely and boot it normally. Verify every required dependency starts without manual intervention.

## 10 — Launch checklist
Test connection, permissions, database persistence, voice, core gameplay, restart behavior, backups, and staff access.

## Next
Continue to **Planning Your FiveM Server**.
