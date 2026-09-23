---
title: "FiveM Resource Troubleshooting"
description: "A structured checklist for resources that will not start or behave correctly."
category: "Troubleshooting"
order: 400
keywords: "FiveM troubleshooting resource failed start command permission dependency"
---

# FiveM Resource Troubleshooting

## Resource not found
Check the folder structure. The manifest should be inside the actual resource folder, not one extra directory deep.

## Resource failed to start
Read the **first relevant error**, not only the final failure line. Look for:
- syntax errors
- missing dependency
- missing export
- missing file
- database connection failure
- invalid configuration

## Command missing
Confirm the resource started successfully and that the command exists in your installed version.

## Permission denied
Check the exact ACE object, principal/group, and whether your permissions CFG executed.

## Works after restart but not on boot
This often points to dependency/start order. Start the dependency first.

## Works for admins only
Check permissions and whether the framework/resource treats administrators differently.

## Still stuck?
Collect:
- resource name and version
- relevant console error
- what you expected
- what actually happened
- steps already tried

Then contact Kruiger Labs Support at **discord.gg/kruigerlabs**.
