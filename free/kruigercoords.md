---
title: "KruigerCoords"
description: "Standalone developer utility for copying the player's vector4 coordinates."
category: "Free Scripts"
order: 110
keywords: "KruigerCoords FiveM free script install configuration troubleshooting"
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
