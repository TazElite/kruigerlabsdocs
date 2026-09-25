---
title: "FiveM Speed Limit Script – KruigerSpeedLimit"
description: "Free FiveM speed limit script documentation with global, class, model and ACE-based vehicle speed limits."
category: "Free Scripts"
order: 140
keywords: "FiveM speed limit script, FiveM speed limiter, KruigerSpeedLimit"
---

# KruigerSpeedLimit

A standalone vehicle speed-limit resource.

## Features
- Global speed limit.
- Configurable maximum up to the limits supported by the resource.
- ACE bypass for authorized users.
- Optional class-based limit mode.

## Installation

```cfg
ensure KruigerSpeedLimit
```

## Configuration
Open the included configuration and choose the global/class behavior required by your server. Configure the documented ACE bypass if staff or specific groups should be exempt.

## Troubleshooting
If a vehicle ignores the limit, check whether the player has the bypass ACE, whether the vehicle class has its own rule, and whether another handling/cruise/speed resource is changing maximum speed.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
