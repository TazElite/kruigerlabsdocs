---
title: "Preparing a Vanta Support Report"
description: "A practical step-by-step Kruiger Labs guide to preparing a vanta support report."
category: "Bots"
order: 631
keywords: "Preparing a Vanta Support Report step by step Kruiger Labs"
---

# Preparing a Vanta Support Report

This guide walks through **Preparing a Vanta Support Report** from preparation through verification, with a rollback path and the checks that matter in a real bots environment.

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


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
