---
title: "Organizing FiveM Resources"
description: "Use bracket folders and predictable naming to keep large servers manageable."
category: "FiveM Servers"
order: 20
keywords: "FiveM resource organization brackets folders nested resource fxmanifest"
---

# Organizing FiveM Resources

As a server grows, the goal is to make it obvious where a resource belongs and what it depends on.

## Recommended categories

```text
resources/
├── [core]          # framework and required core resources
├── [database]      # database adapters when applicable
├── [voice]         # voice resources
├── [standalone]    # independent scripts
├── [kruiger]       # Kruiger Labs resources
├── [maps]          # maps/MLO resources
├── [vehicles]      # vehicle resources
├── [eup]           # clothing/EUP resources
└── [dev]           # development tools you intentionally run
```

You do not need every category. Create only categories that help your server.

## Good rules
1. Keep one resource per resource folder.
2. Keep the original resource folder name unless renaming is supported.
3. Do not nest bracket folders unnecessarily.
4. Keep dependencies near the top of the startup order.
5. Remove abandoned duplicate copies such as `resource-old`, `resource-new2`, and `resource-final-final`.
6. Use version control for text configuration and scripts you are allowed to store.

## Moving an existing resource
1. Stop the server or stop the resource.
2. Move the **whole** resource folder into its category.
3. Verify `fxmanifest.lua` is still directly inside the resource folder.
4. Check `server.cfg` for old paths or renamed resource references.
5. Start the server and watch the console.
6. Test the resource in-game.

## Common mistake: an extra folder
Wrong:

```text
resources/[kruiger]/KruigerHandsUp/KruigerHandsUp/fxmanifest.lua
```

Correct:

```text
resources/[kruiger]/KruigerHandsUp/fxmanifest.lua
```

If FiveM cannot find the manifest where expected, the resource will not load correctly.
