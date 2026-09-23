---
title: "KruigerChat"
description: "Commands, chat tags, configuration, conflict removal, permissions, and troubleshooting for KruigerChat."
category: "Paid Scripts"
order: 220
keywords: "KruigerChat configuration commands ACE permissions troubleshooting"
---

# KruigerChat

KruigerChat is the Kruiger Labs custom FiveM chat component.

## Established commands
The package includes the following chat-facing command set:

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

The exact formatting/access of each command follows the configuration in your installed release.

## Before installing
A server should have one intended primary chat implementation. If the default or another replacement chat is active at the same time, you can see duplicate UI/messages or conflicting behavior.

Do not remove your existing chat until you have a rollback copy.

## Installation
1. Upload KruigerChat.
2. Configure chat presentation and enabled features.
3. Configure chat tags/department mappings.
4. Configure permissions for administrative settings.
5. Stop the chat implementation KruigerChat replaces, when applicable.
6. Ensure KruigerChat.
7. Test every enabled command.
8. Test with at least two players.

## Chat tags
Chat Tags are configurable. Keep tag identifiers consistent with your server permissions/departments. `/chattag` is part of the established command set, while `/chatsettings` exposes the user/settings workflow included by the package.

## Command testing
Test each enabled command for:
- correct name/display
- correct range/audience
- permission behavior
- formatting
- escaping/long messages
- two-player visibility

## Troubleshooting
### Two chat boxes or duplicate messages
Another chat resource is still running. Identify both resources before disabling anything.

### A command is unknown
Confirm KruigerChat started and that the command is enabled in the installed configuration.

### Tag is wrong
Check overlapping permissions and the tag/department identifier assigned to the user.

### UI loads but input is broken
Inspect the FiveM client console for NUI errors and confirm no other chat resource is capturing focus.
