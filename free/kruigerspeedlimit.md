---
title: "KruigerSpeedLimit"
description: "Configurable global vehicle speed limit with ACE bypass and optional class limits."
category: "Free Scripts"
order: 140
keywords: "KruigerSpeedLimit FiveM free script install configuration troubleshooting"
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
