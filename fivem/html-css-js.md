---
title: "HTML/CSS/JS for FiveM NUI"
description: "A practical step-by-step Kruiger Labs guide to html/css/js for fivem nui."
category: "FiveM Servers"
order: 59
keywords: "HTML/CSS/JS for FiveM NUI step by step Kruiger Labs"
---

# HTML/CSS/JS for FiveM NUI

This guide walks through **HTML/CSS/JS for FiveM NUI** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## How NUI fits together

A typical NUI resource has an `fxmanifest.lua`, client/server code where needed, and web assets such as HTML/CSS/JS. The manifest declares `ui_page` and the files clients need.

## Minimal manifest shape

```lua
fx_version 'cerulean'
game 'gta5'
ui_page 'web/index.html'
files { 'web/index.html', 'web/style.css', 'web/app.js' }
client_script 'client.lua'
```

## Opening and closing

Your Lua/JS client code controls focus and messages. Always provide a reliable close path; a stuck focus state can make the player appear frozen.

## Callbacks

Treat data coming from the browser UI as untrusted input. If a callback ultimately changes authoritative game/server state, validate the action again on the server.

## Debugging

Use the FiveM/client console and NUI developer tooling where available. Check file paths, manifest `files`, browser-console errors, callback names and focus state.
