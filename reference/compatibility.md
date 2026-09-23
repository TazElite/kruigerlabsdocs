---
title: "Compatibility & Dependency Checklist"
description: "A repeatable compatibility check before installing or updating a FiveM resource."
category: "Reference"
order: 106
keywords: "Compatibility & Dependency Checklist"
---

# Compatibility & Dependency Checklist
Before installation record:
- resource version
- FXServer artifact/build
- framework and version, or Standalone
- database adapter/version if used
- required resources/libraries
- optional integrations
- resource names that must remain unchanged
- resources it replaces/conflicts with
- required ACEs
- SQL migrations
- required map/postal/assets
- restart/reconnect requirements

## Result
Mark each item **Confirmed**, **Not applicable**, or **Unknown**. Resolve every Unknown that can prevent startup before production deployment.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
