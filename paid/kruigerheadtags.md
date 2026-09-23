---
title: "KruigerHeadtags"
description: "Configure Headtags and Gangtags, ACE permissions, user controls, departments, and troubleshooting."
category: "Paid Scripts"
order: 240
keywords: "KruigerHeadtags configuration commands ACE permissions troubleshooting"
---

# KruigerHeadtags

KruigerHeadtags provides configurable overhead **Headtags** and **Gangtags**.

## Established commands

```text
/headtag
/headtags
/gangtag
/gantag
/headtagsettings
/showheadtagself
```

`/gantag` is retained as an established command spelling/alias from the package work.

## Permissions
The established ACE namespaces are:

```text
headtag.kruiger.*
gangtag.kruiger.*
```

Use the exact action/tag ACE objects shipped in your installed release beneath those namespaces.

## Adding a headtag
1. Open the editable tag configuration supplied with your release.
2. Choose a unique internal tag identifier.
3. Add the display label/style values supported by the config.
4. Associate the tag with the appropriate permission/department behavior.
5. Add the corresponding documented ACE to the intended group.
6. Restart/reload as required by the release.
7. Test with an account that has the ACE.
8. Test with an account that does not.

## Adding a department
Use one stable internal department identifier across the suite. A display name can be friendly (`San Andreas Highway Patrol`) while the internal key remains stable (`sahp`, for example).

## Gangtags
Gangtags have their own `gangtag.kruiger.*` permission namespace. Do not grant a broad wildcard to ordinary users when a narrower tag permission is sufficient.

## User controls
Use `/headtagsettings` for the settings workflow and `/showheadtagself` for the self-visibility behavior included in the package.

## Troubleshooting
### No headtag
Check the exact ACE, group inheritance, configuration identifier, and whether the headtag resource is running.

### Wrong headtag
Look for multiple matching ACEs/tags and the priority/order behavior defined by your version.

### Gangtag works but headtag does not
Treat them separately: they use separate namespaces.

### Tag does not update after permission change
Reconnect/reload according to your permission integration and test whether the underlying principal was actually updated.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
