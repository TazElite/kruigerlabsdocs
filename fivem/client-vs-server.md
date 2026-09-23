---
title: "Client Scripts vs Server Scripts"
description: "Understand where FiveM code runs and why security-sensitive decisions belong on the server."
category: "FiveM Servers"
order: 6
keywords: "FiveM Client Scripts vs Server Scripts beginner step by step"
---

# Client Scripts vs Server Scripts

Understand where FiveM code runs and why security-sensitive decisions belong on the server.

## Client

Client scripts run for each connected player and interact with that player's game. Treat client-supplied values as untrusted.

## Server

Server scripts run on FXServer and are the correct place for authoritative validation, persistence, permissions, and shared state.

## Shared

Shared scripts load on both sides. Use them for constants/configuration that truly belongs on both sides; never put secrets in client/shared files.

## Rule

A client can request an action. The server should decide whether the action is allowed.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
