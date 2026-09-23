---
title: "Updating Resources Safely"
description: "Update FiveM resources with backups, changelog checks, and controlled restarts."
category: "FiveM Servers"
order: 80
keywords: "FiveM update resource backup restart changelog rollback"
---

# Updating Resources Safely

## Before updating
1. Read the release notes/changelog.
2. Back up the current resource and its configuration.
3. Check for config changes or migrations.
4. Check whether dependencies changed.

## Replace code carefully
Do not blindly overwrite a customized config with a new default. Compare the new configuration options with your existing file.

## Restart
For a simple independent resource, a controlled resource restart may be enough:

```text
restart ResourceName
```

Some framework, database, map, or shared-library updates are safer during a full maintenance restart. Follow that product's instructions.

## Roll back
If the update fails:
1. Stop the affected resource.
2. Restore the known-good version.
3. Restore the compatible configuration.
4. Start it and verify.
5. Review the failed update before retrying.
