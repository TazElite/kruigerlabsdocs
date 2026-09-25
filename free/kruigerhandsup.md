---
title: "FiveM Hands Up & Kneel Script – KruigerHandsUp"
description: "Free FiveM hands up and kneel script documentation with /handsup, /huk, configurable controls and exports."
category: "Free Scripts"
order: 100
keywords: "FiveM hands up script, FiveM kneel script, FiveM surrender script, KruigerHandsUp"
---

# KruigerHandsUp

A lightweight standalone surrender resource.

## Features
- Press **X** by default to toggle hands up.
- `/handsup` toggles hands up/down.
- `/huk` toggles the hands-on-knees stance.
- `/huk` keeps the player's currently selected weapon rather than intentionally switching it away.
- Combat controls are blocked while surrendered.
- The stance cancels when conditions such as death, ragdoll, or entering a vehicle make the animation inappropriate.
- Client exports are available for integrations.

## Installation
1. Download or clone the resource.
2. Place `KruigerHandsUp` inside your resources directory, for example `resources/[kruiger]/KruigerHandsUp`.
3. Add:

```cfg
ensure KruigerHandsUp
```

4. Restart the server or start the resource.

## Commands and controls
| Input | Action |
|---|---|
| `X` | Toggle hands up (default key mapping) |
| `/handsup` | Toggle hands up |
| `/huk` | Toggle hands on knees |

Players can change a registered FiveM key mapping in their FiveM keybind settings.

## Configuration
Open `config.lua` to review the default key, command, animation, and controls blocked while surrendered. Keep the resource name unchanged if another script uses its exports.

## Exports

```lua
local handsUp = exports['KruigerHandsUp']:IsHandsUp()
local huk = exports['KruigerHandsUp']:IsHUK()
local stance = exports['KruigerHandsUp']:GetSurrenderStance()
```

## Troubleshooting
### X does nothing
Check that the resource started, `/handsup` works, and another key mapping is not conflicting. Review FiveM keybind settings.

### `/huk` does nothing
Confirm you are on foot and in a state where the animation can play. Check the client console for animation/resource errors.

### Weapon behavior is wrong
Test with the exact weapon and other weapon/inventory resources enabled. Another resource can independently force weapon switching or animations.

### Resource will not start
Confirm `fxmanifest.lua` is directly inside the `KruigerHandsUp` folder and that you do not have an extra nested folder.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
