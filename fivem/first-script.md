---
title: "Your First FiveM Script"
description: "Create, start, test, stop, edit, and restart a tiny Lua resource."
category: "FiveM Servers"
order: 4
keywords: "FiveM Your First FiveM Script beginner step by step"
---

# Your First FiveM Script

Create, start, test, stop, edit, and restart a tiny Lua resource.

## Create the resource

Inside your server's `resources` directory create `[local]/helloKruiger/`. Inside it create `fxmanifest.lua` and `client.lua`.

## Manifest

```lua
fx_version 'cerulean'
game 'gta5'
author 'YourName'
description 'My first resource'
version '1.0.0'
client_script 'client.lua'
```

## Client script

```lua
print('helloKruiger loaded')
```
Save both files.

## Start it

In the server console run `refresh`, then `ensure helloKruiger`. Alternatively use txAdmin's resource controls. Open F8 in FiveM and confirm the message appears.

## Make a change

Change the printed text, save, then run `restart helloKruiger`. This edit → restart → verify loop is the foundation of resource development.

## Make it survive reboot

Add `ensure helloKruiger` to the appropriate startup configuration, then perform a full cold boot to prove it starts automatically.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
