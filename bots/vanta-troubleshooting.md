---
title: "Vanta Troubleshooting"
description: "A symptom-first troubleshooting guide for commands, dashboard, roles, verification, tickets, music, logs and database-backed features."
category: "Bots"
order: 360
keywords: "Vanta Troubleshooting Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Troubleshooting
Start with the symptom instead of reinstalling the bot.

## Slash command missing
Use `/help` to confirm the current command structure. Confirm Vanta is installed and Discord command registration has completed.

## “Module is disabled” or command disabled
A server manager can enable the module/command from the Vanta dashboard.

## Role action fails
Check Vanta's Discord permission and role hierarchy.

## Dashboard is stale
Refresh the guild data/page. Vanta's dashboard was designed to fetch fresh server data rather than require logout/login after changes.

## Verification link expired
Generate a new link. Verification links are designed to expire after 5 minutes.

## Ticket cannot create a channel
Check channel/category permissions and Vanta's ability to create/manage channels in the configured category.

## Logs stopped
Check the configured channel still exists and Vanta can view/send/embed there.

## Music fails
Try another track/provider result and check provider/status information.

## Database-backed feature fails
A healthy Discord connection does not prove MySQL-backed features are healthy. Report the exact error and feature.

## Still stuck
Collect the server ID, Vanta version, command/feature, exact error, screenshots/log excerpt, and what you already tried. Then use Kruiger Labs Support.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
