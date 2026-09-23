---
title: "Kruiger Ultimate Suite"
description: "End-to-end setup for HUD, Headtags, Priority, Duty and Chat as one coordinated Kruiger Labs FiveM suite."
category: "Paid Scripts"
order: 250
keywords: "Kruiger Ultimate Suite configuration commands ACE permissions troubleshooting"
---

# Kruiger Ultimate Suite

Kruiger Ultimate Suite combines:

- **KruigerHUD**
- **KruigerHeadtags**
- **KruigerPriority**
- **KruigerDuty**
- **KruigerChat**

The suite is most reliable when you configure the shared concepts once and use the same identifiers everywhere.

## Established command set

### HUD
```text
/hud
/postal [code]
/togglespeed
```

### Headtags / Gangtags
```text
/headtag
/headtags
/gangtag
/gantag
/headtagsettings
/showheadtagself
```

### Duty
```text
/duty
/dutysetup
```

### Priority
```text
/priority
```

### Chat
```text
/me
/gme
/do
/social
/sms
/ad
/chatsettings
/chattag
```

Established controls include **E**, **L**, and **F1**, depending on the component/configuration.

## Permission namespaces
The package work established these namespaces:

```text
headtag.kruiger.*
gangtag.kruiger.*
kruiger.priority.*
```

Use the exact granular ACEs shipped with your release.

## Recommended installation order
1. Back up the server.
2. Install the required postal map/dependencies.
3. Upload all suite components.
4. Decide your internal department identifiers.
5. Configure those departments consistently across components.
6. Configure Headtags/Gangtags.
7. Configure duty locations.
8. Configure priority statuses/cooldown.
9. Configure Chat Tags and chat behavior.
10. Configure ACE permissions.
11. Configure optional Discord logging.
12. Disable conflicting HUD/chat/priority/headtag resources only when ready.
13. Start dependencies before suite resources.
14. Cold boot.
15. Test each component separately.
16. Test cross-component behavior.

## Department planning worksheet
Before editing configs, make a small table:

| Internal ID | Display name | Duty access | Headtag | Chat tag |
|---|---|---|---|---|
| `sahp` | San Andreas Highway Patrol | configured group | configured tag | configured tag |

Use your own identifiers. The important part is consistency.

## Priority statuses
The established states are **Available**, **Active**, **On Hold**, and **Cooldown**.

## Postal
The HUD package was designed around the recommended Big Daddy Scripts Postal Map. Validate the map before troubleshooting postal alignment.

## Logging
Optional Discord logging is part of the suite configuration work. Keep webhooks private and use separate logging destinations when that helps operations.

## Full acceptance test
Do not call the suite finished because it starts. Test:
1. HUD on foot.
2. HUD in multiple vehicles.
3. Postal command.
4. Headtag authorized/unauthorized.
5. Gangtag authorized/unauthorized.
6. Duty in/out.
7. Duty setup permission.
8. Every priority state.
9. Cooldown.
10. Every enabled chat command.
11. Chat tag.
12. User settings.
13. Reconnect synchronization.
14. Full cold boot.
15. Multi-player visibility.
16. Console/client errors.

## Troubleshooting the suite
When several features fail, disable the assumption that “the suite is one problem.” Verify each component individually, then shared identifiers, permissions, start order, and conflicts.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
