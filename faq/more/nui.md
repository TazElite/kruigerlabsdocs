---
title: "NUI FAQ"
description: "A practical step-by-step Kruiger Labs guide to nui faq."
category: "FAQ"
order: 911
keywords: "NUI FAQ step by step Kruiger Labs"
---

# NUI FAQ

This guide walks through **NUI FAQ** from preparation through verification, with a rollback path and the checks that matter in a real faq environment.

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


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
