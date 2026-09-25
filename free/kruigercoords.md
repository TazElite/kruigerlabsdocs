---
title: "FiveM Coordinates Script – KruigerCoords"
description: "Free FiveM coordinates script documentation for copying vector4 coordinates and heading with /coords."
category: "Free Scripts"
order: 110
keywords: "FiveM coords script, FiveM coordinates script, FiveM vector4, KruigerCoords"
---

# KruigerCoords

A small standalone developer utility for quickly capturing FiveM coordinates.

## Installation
1. Place `KruigerCoords` in your resources directory.
2. Add:

```cfg
ensure KruigerCoords
```

3. Restart/start the resource.

## Usage
Use `/coords` in-game to capture the player's current position and heading as a `vector4` value for development/configuration work.

## Troubleshooting
If the command is missing, confirm the resource started and check the console for manifest or Lua errors. If copying does not work as expected, verify the distributed version's clipboard/UI behavior and check the client console.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
