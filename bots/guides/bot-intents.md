---
title: "Discord Gateway Intents"
description: "A practical step-by-step Kruiger Labs guide to discord gateway intents."
category: "Bots"
order: 618
keywords: "Discord Gateway Intents step by step Kruiger Labs"
---

# Discord Gateway Intents

This guide walks through **Discord Gateway Intents** from preparation through verification, with a rollback path and the checks that matter in a real bots environment.

## Before setup

Confirm the bot is the official application, choose the correct server, and understand which Discord permissions the feature actually requires. Avoid Administrator when narrower permissions are sufficient.

## Role hierarchy

For role management/moderation, place the bot role above roles it must manage. Discord will reject actions outside the bot's hierarchy even if its configuration looks correct.

## Configure

Use the bot's slash commands/dashboard for the feature. Save one small configuration first and test it before building a large production setup.

## Test as a member

Administrator accounts can hide permission problems. Test with a normal member and, where relevant, a normal staff role.

## Troubleshoot

Capture the command, exact response, server ID, bot version/status, relevant role/channel hierarchy and a screenshot. Never send the bot token.
