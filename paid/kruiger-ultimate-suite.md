---
title: "Kruiger Ultimate Suite"
description: "Combined package containing the Kruiger HUD, Headtags, Duty, Chat, and Priority components."
category: "Paid Scripts"
order: 250
keywords: "Kruiger Ultimate Suite paid FiveM install setup troubleshooting"
---

# Kruiger Ultimate Suite

The Ultimate Suite combines the major Kruiger FiveM packages into one coordinated server offering.

## Included components
- KruigerHUD
- KruigerHeadtags
- KruigerDuty
- KruigerChat
- KruigerPriority

## Recommended setup order
1. Back up the server.
2. Remove/disable conflicting replacements only after identifying what each Kruiger component replaces.
3. Install all required dependencies.
4. Configure shared department names/identifiers consistently.
5. Configure permissions.
6. Start the components in the order documented by the delivered suite.
7. Test HUD → headtags → duty → chat → priority.
8. Test with a normal member, staff member, and multiple departments.

## Why consistent identifiers matter
If one component calls a department `sahp` while another configuration expects a different identifier, integrations can appear broken even though both resources started successfully.

## Troubleshooting
Test one component at a time. A console showing every resource as started does not guarantee cross-resource configuration is correct. Compare department identifiers, permissions, and dependency order first.
