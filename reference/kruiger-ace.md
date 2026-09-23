---
title: "Kruiger ACE Reference"
description: "Central reference for established Kruiger permission namespaces."
category: "Reference"
order: 102
keywords: "Kruiger ACE Reference"
---

# Kruiger ACE Reference
Established product namespaces include:

```text
headtag.kruiger.*
gangtag.kruiger.*
kruiger.priority.*
```

The wildcard notation describes a **namespace**, not an instruction to grant `*` broadly. Use the exact granular ACE objects shipped with your installed version.

## Recommended pattern
```cfg
# Define narrow product ACEs here.
# add_ace group.example exact.permission allow

# Assign trusted principals/groups separately.
# add_principal identifier.fivem:YOUR_ID group.example
```

Load permission definitions before resources that inspect them during startup. Test both an authorized and unauthorized account.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
