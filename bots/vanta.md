---
title: "Vanta"
description: "Public Discord bot documentation covering setup, dashboard, verification, tickets, profiles, music, and troubleshooting."
category: "Bots"
order: 300
keywords: "Vanta Discord bot dashboard verification tickets profiles music commands troubleshooting"
---

# Vanta

Vanta is the public Kruiger Labs Discord bot. This page is the Kruiger Labs documentation entry point for Vanta.

## Getting started
1. Add Vanta to the Discord server using the official Vanta invite flow.
2. Make sure the bot role is high enough for the roles/features you want Vanta to manage.
3. Complete server setup using Vanta's commands or dashboard.
4. Configure only the modules your community needs.
5. Test moderation, tickets, verification, and logging with a non-administrator test account where possible.

## Dashboard
The Vanta dashboard provides server-specific configuration. If you change a Discord channel or role outside Vanta, refresh/reload the relevant dashboard data before assuming the old value is still valid.

## Verification
Vanta supports a verification flow using CAPTCHA/role assignment. Confirm the bot can manage the configured Verified/Unverified roles and that its role is above roles it must assign.

## Tickets
Configure ticket panels, categories, support roles, labels/emojis, ticket prefixes, and welcome behavior. Test creating and closing a ticket before publishing the panel broadly.

## Profiles
Vanta profiles support privacy controls. Users who choose private visibility should not be presented as public-directory profiles.

## Music
Music availability depends on the providers and access rules enabled in the current Vanta release. Provider restrictions, track availability, and regional/access rules can affect whether a requested track can be played.

## Troubleshooting
### Dashboard changes do not appear
Refresh the server data and confirm the bot still has access to the selected Discord objects.

### Roles are not assigned
Move Vanta's bot role above the role it needs to manage and verify Manage Roles permission.

### Slash command is missing
Confirm Vanta is installed in the server, the command is available in the current release, and Discord has completed command propagation.

### Music request fails
Try another track and check Vanta's current provider/status information. A provider can reject or restrict an individual track even while the bot itself is online.

## Official resources
Use the official Vanta website for live Vanta-specific service information and the Kruiger Labs support server for support that cannot be resolved through troubleshooting.
