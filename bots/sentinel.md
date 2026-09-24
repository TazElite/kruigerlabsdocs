---
title: "Kruiger Sentinel"
description: "Kruiger Labs network-wide enforcement, case management, evidence review, public records and ban synchronization."
category: "Bots"
order: 320
keywords: "Kruiger Sentinel Discord bot network bans blacklists cases evidence public records sync"
---

# Kruiger Sentinel

Kruiger Sentinel is Kruiger Labs' internal network-wide enforcement and case-management bot. It provides a centralized system for reviewed blacklists, network bans, evidence, case notes, audit history, public enforcement records, and synchronization across authorized Kruiger Labs Discord communities.

Sentinel is intended for **authorized Kruiger Labs communities**. It is not a public moderation bot.

## Core features
- Centralized cases using IDs such as `KL-#########`
- Blacklist and network-ban request/review workflows
- Evidence and case-note history
- Reviewer, administrator, and owner permission levels
- Network-wide ban enforcement across authorized servers
- Public enforcement records for approved actions
- Removal history for unbans and unblacklists
- Audit logging and per-server channel configuration
- Network-ban synchronization
- Public-record refresh tools

## Commands

### Case and enforcement
- `/request blacklist` — submit a blacklist request.
- `/request ban` — submit a network-ban request.
- `/unblacklist` — remove an active blacklist while preserving history.
- `/unban` — remove an active network ban across authorized servers.
- `/find user` — find records associated with a Discord user.
- `/find case` — retrieve a case by case number.
- `/sync` — synchronize active network bans across authorized servers.

### Sentinel administration
- `/sentinel setup`
- `/sentinel status`
- `/sentinel server add/remove/list`
- `/sentinel channel set/view/reset`
- `/sentinel role requester add/remove`
- `/sentinel role reviewer add/remove`
- `/sentinel role admin add/remove`
- `/sentinel reason add/remove/list`
- `/sentinel settings`
- `/sentinel config`
- `/sentinel refresh-public-records`

> Command availability depends on staff permissions and the installed Sentinel release.

## Review workflow
Requests are submitted for staff review before becoming active enforcement records. Approved blacklists and bans are recorded centrally and can be published to each configured public-record channel. Denied requests remain internal.

Removing enforcement does not erase the original case. Sentinel preserves the case history and updates the enforcement state.

## Network synchronization
`/sync` checks active Sentinel network bans against authorized servers and attempts to bring enforcement back into sync. Results are handled per server so one failure does not block the rest of the network.

## Public records
Only approved enforcement actions are published. Public records can contain the case number, affected Discord user, enforcement type, reason, status, issue date, scope, and approved public evidence when applicable.

Pending requests, denied requests, private staff notes, reviewer information, audit data, and non-public evidence remain internal.

## Case numbers
Sentinel uses the unified format:

`KL-#########`

## Security
Never publish `.env` files, bot tokens, database passwords, connection strings, private evidence, or other production secrets.

## Support
Sentinel is maintained by **Kruiger Labs LLC** for authorized Kruiger Labs communities.

## Document status
**Last reviewed:** September 2026  
**Product:** Kruiger Sentinel  
**Availability:** Internal / authorized Kruiger Labs communities  
**Version note:** Check commands and behavior against the installed Sentinel release before production changes.
