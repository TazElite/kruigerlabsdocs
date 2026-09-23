---
title: "Vanta Dashboard"
description: "Detailed guide to Vanta's guild dashboard, modules, commands, settings, tickets, logs, music and archives."
category: "Bots"
order: 310
keywords: "Vanta Dashboard Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Dashboard
After Discord login, the guild picker should show servers available through Vanta's authenticated guild access.

## Sections
- **Overview** — server/Vanta summary.
- **Modules** — enable/disable feature modules.
- **Commands** — enable/disable commands per guild.
- **General** — general server configuration.
- **Welcome & Leave** — member arrival/departure behavior.
- **Music** — guild music configuration.
- **Fun** — fun feature settings.
- **Games** — game feature settings.
- **Tickets** — ticket configuration.
- **Logs** — logging configuration.
- **Custom Voice** — custom voice configuration.
- **Ticket Archives** — archived ticket/transcript access.

## Module and command switches
A disabled module blocks commands belonging to it. An individually disabled command is also blocked. Vanta reports that it is disabled rather than pretending the command failed.

For backwards compatibility, missing module/command switches in stored settings are treated as enabled.

## Changes do not appear
Refresh the dashboard/server data, verify the Discord object still exists, and confirm Vanta can see/manage the selected role/channel.
