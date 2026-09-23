---
title: "Your First Client ↔ Server Event"
description: "Send a request from a client to the server and return a response safely."
category: "FiveM Servers"
order: 7
keywords: "FiveM Your First Client ↔ Server Event beginner step by step"
---

# Your First Client ↔ Server Event

Send a request from a client to the server and return a response safely.

## Server file

Add `server.lua` and declare it in the manifest. Register a named server event and validate what the client sends before acting.

## Client request

Use FiveM's event APIs to send a small request to the server. Keep event names namespaced, for example `kruiger_tutorial:hello`.

## Security

Never create a server event that blindly trusts money, roles, item counts, permissions, coordinates, or target IDs supplied by a client.

## Test

Use two clients when possible so you learn the difference between one player's local state and shared server state.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
