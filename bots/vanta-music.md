---
title: "Vanta Music"
description: "How Vanta music works, provider limitations, queues, playback controls, and provider-specific failures."
category: "Bots"
order: 345
keywords: "Vanta Music Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Music
Vanta's music system is designed around search/playback, queues and standard controls such as play/pause, skip, repeat and shuffle.

Provider availability can change independently of Vanta. A bot being online does not mean every provider or track is available.

## Audius
Vanta has evaluated/used Audius API integration for search, metadata and authorized streaming. Audius access/licensing can vary by track. Attribution and access requirements should be respected.

## Troubleshooting a failed track
1. Try another track.
2. Determine whether search works but playback fails.
3. Check whether the provider requires access/gating.
4. Check the current Vanta status.
5. Do not assume a provider-wide outage from one unavailable track.

Vanta should not permanently download provider tracks as part of normal playback.
