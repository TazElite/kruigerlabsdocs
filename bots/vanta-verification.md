---
title: "Vanta Verification"
description: "Set up Vanta verification, CAPTCHA, roles, panels, web verification, expiration, and troubleshooting."
category: "Bots"
order: 315
keywords: "Vanta Verification Vanta Discord bot setup dashboard troubleshooting"
---

# Vanta Verification
Vanta's verification system is configured through:

```text
/setup verification
```

## Flow
The established verification design supports a public verification panel and CAPTCHA/web verification. Verification links are **account-bound** and expire after **5 minutes**.

Web verification uses Turnstile in the established system design.

## Setup checklist
1. Create/choose Verified and Unverified roles.
2. Move Vanta above roles it must assign/remove.
3. Run `/setup verification`.
4. Select the intended verification channel/panel configuration.
5. Configure the verification method available in the current release.
6. Publish the panel.
7. Test from a normal account.
8. Confirm expired links cannot be reused.
9. Confirm a link generated for one account cannot verify another.

## Troubleshooting
If verification succeeds but the role does not change, inspect Discord role hierarchy and Manage Roles permission first.
