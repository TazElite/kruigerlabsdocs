---
title: "FiveM Scene & Evidence Script – KruigerScenes"
description: "Documentation for KruigerScenes, a free synchronized FiveM scene and evidence-description script with 3D text, persistence, presets and ACE permissions."
category: "Free Scripts"
order: 170
keywords: "FiveM scene script, FiveM evidence script, FiveM 3D text scene, KruigerScenes"
---

# KruigerScenes

KruigerScenes is a free standalone synchronized scene and evidence-description resource for FiveM roleplay servers.

## Features
- `/scene` creation menu and `/scenes` manager
- World raycast placement
- Evidence and roleplay presets
- Inspect-only, 3D text, or combined display modes
- Timed and persistent scenes
- ACE permission controls
- No ESX or QBCore dependency

## Installation
1. Place `KruigerScenes` in your FiveM resources folder.
2. Add `ensure KruigerScenes` to `server.cfg`.
3. Configure the ACE permissions you want.
4. Restart the resource or server.

## ACE permissions
```cfg
add_ace group.leo kruiger.scenes.create allow
add_ace group.fire kruiger.scenes.create allow
add_ace group.admin kruiger.scenes.permanent allow
add_ace group.admin kruiger.scenes.manage allow
```

## Usage
Use `/scene` to create a scene and `/scenes` to manage active scenes. Permanent scenes persist to `scenes.json`; timed scenes expire automatically.

## Source
The free release is available from the official Kruiger Labs GitHub repository: `TazElite/KruigerScenes`.
