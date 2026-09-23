---
title: "Vanta Auto Replies"
description: "Create, list and remove automatic replies with matching, channel restrictions, cooldowns and mention protection."
category: "Bots"
order: 330
keywords: "Vanta Auto Replies Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Auto Replies
Auto replies live under `/config`, not a separate top-level autoresponder command family.

```text
/config autoreply-add
/config autoreply-list
/config autoreply-remove
```

The established system supports matching modes, channel restrictions, cooldowns and mention protection, with a **50-rule limit**.

## Setup
Create a narrowly matched rule first, restrict it to the intended channels where appropriate, set a cooldown that prevents spam, and test both matching and non-matching messages.

## Troubleshooting
If a rule never triggers, check matching mode, channel restrictions, module/command state, and whether the triggering message satisfies the configured match.
