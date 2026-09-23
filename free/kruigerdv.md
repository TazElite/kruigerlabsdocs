---
title: "KruigerDV"
description: "Standalone vehicle deletion utility for the current or nearest vehicle."
category: "Free Scripts"
order: 120
keywords: "KruigerDV FiveM free script install configuration troubleshooting"
---

# KruigerDV

A standalone `/dv` vehicle deletion resource.

## Installation

```cfg
ensure KruigerDV
```

Place the full resource folder in `resources` first.

## Usage
`/dv` deletes the vehicle the player is currently using or, when supported by the current situation, the nearest applicable vehicle.

## Configuration
Review the included configuration before production use, especially any permission or distance options present in your release.

## Troubleshooting
If a nearby vehicle is not deleted, test while seated in a vehicle and check client/server console output. Confirm another vehicle-management or anti-cheat resource is not blocking deletion.
