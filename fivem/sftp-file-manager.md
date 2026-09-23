---
title: "SFTP & File Manager"
description: "Upload, move, edit, and back up server files without creating nested-resource or partial-upload problems."
category: "FiveM Servers"
order: 75
keywords: "SFTP & File Manager FiveM step by step"
---

# SFTP & File Manager
Most hosts provide a browser file manager, SFTP, or both.

## Browser file manager
Good for small edits and quick uploads. Large folder operations may be slower.

## SFTP
Useful for moving many files and keeping the folder tree visible.

## Upload checklist
1. Stop the resource when replacing important files.
2. Upload the **complete** resource.
3. Check for an accidental double folder.
4. Confirm the manifest is directly inside the resource folder.
5. Preserve config backups before overwriting.
6. Start/restart and read the console.

## Success check
Your final path looks like:

```text
resources/[category]/ResourceName/fxmanifest.lua
```

—not `ResourceName/ResourceName/fxmanifest.lua`.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
