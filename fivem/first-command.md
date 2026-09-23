---
title: "Creating Your First /command"
description: "Register a simple client command and understand arguments before building larger scripts."
category: "FiveM Servers"
order: 5
keywords: "FiveM Creating Your First /command beginner step by step"
---

# Creating Your First /command

Register a simple client command and understand arguments before building larger scripts.

## Code

Replace your `client.lua` with:
```lua
RegisterCommand('hello', function(source, args)
    local name = args[1] or 'player'
    print(('Hello %s!'):format(name))
end, false)
```

## Test

Restart the resource. In FiveM run `/hello` and `/hello Kruiger`, then inspect F8.

## What you learned

`RegisterCommand` creates a command, `args` contains words typed after the command, and the final `false` means this example is not restricted by the built-in command ACE flag.

## Next

Do not put sensitive authority only on the client. Continue into client/server separation and server-side validation.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
