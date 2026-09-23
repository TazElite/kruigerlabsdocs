---
title: "FiveM Console Quick Reference"
description: "Quick resource lifecycle and diagnostic commands for server owners."
category: "Reference"
order: 104
keywords: "FiveM Console Quick Reference"
---

# FiveM Console Quick Reference
```text
refresh
start ResourceName
stop ResourceName
restart ResourceName
ensure ResourceName
```

- `refresh` rescans resource manifests.
- `start` starts a stopped resource.
- `stop` stops it.
- `restart` stops then starts it.
- `ensure` starts it if stopped and restarts it if already running.

A manually successful `ensure` does **not** prove correct cold-boot start order. Always test a full server restart before production.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
