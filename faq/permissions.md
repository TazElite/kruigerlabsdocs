---
title: "Permissions FAQ"
description: "Answers about ACE permissions, principals, groups, setup commands and role hierarchy."
category: "FAQ"
order: 505
keywords: "Permissions FAQ frequently asked questions"
---

# Permissions FAQ
<details><summary><strong>What is an ACE?</strong></summary><p>An ACE is a permission rule. Resources can check named ACE objects to decide whether a principal is allowed to perform an action.</p></details>
<details><summary><strong>Why does an admin command say permission denied?</strong></summary><p>Verify the exact ACE object, the user's principal/group inheritance, and that the permissions file executes before the resource needs it.</p></details>
<details><summary><strong>Can I put ACEs in permissions.cfg?</strong></summary><p>Yes. Load it from <code>server.cfg</code> with <code>exec permissions.cfg</code>.</p></details>
<details><summary><strong>Should I grant wildcards to everyone?</strong></summary><p>No. Prefer the narrowest permission needed for the role.</p></details>


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
