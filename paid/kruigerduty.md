---
title: "FiveM Duty Script – KruigerDuty"
description: "FiveM duty script documentation for KruigerDuty: departments, duty locations, clock-in workflow, permissions, logging and setup."
category: "Paid Scripts"
order: 210
keywords: "FiveM duty script, FiveM clock in script, FiveM department duty, KruigerDuty"
---

# KruigerDuty

KruigerDuty is the duty/clock-in component of the Kruiger server package. It is intended to let configured departments use controlled duty locations rather than hard-coding one department into the resource.

## Commands and interaction
The established duty commands are:

```text
/duty
/dutysetup
```

The duty interaction uses **E** where the configured duty interaction requires it.

`/duty` is the normal duty workflow. `/dutysetup` is the administrative setup workflow and should be restricted to trusted administrators.

## Installation
1. Upload the complete resource.
2. Read the included editable configuration.
3. Configure departments first.
4. Configure duty locations for those departments.
5. Configure administrative permissions.
6. Configure optional Discord logging if your release includes it.
7. Add ACE/configuration **before** `ensure KruigerDuty`.
8. Start the server.
9. Create/test one duty location before creating the rest.

## Departments
Use consistent internal identifiers across the Kruiger suite. For example, if the internal department identifier is `sahp`, do not call the same department `statepolice` in another component unless the configuration explicitly maps the two.

For each department, document:
- internal identifier
- display name
- allowed ranks/groups
- duty locations
- headtag/chat behavior when integrated
- logging destination if applicable

## Duty locations
When adding a location:
1. Stand exactly where the interaction should occur.
2. Capture the required coordinates.
3. Add them using the configuration/setup method in your installed version.
4. Set the intended department/access.
5. Restart/reload only as documented.
6. Test the marker/interaction from a normal department account.
7. Test an account that should **not** have access.

## Logging
The package design includes optional Discord logging. Treat webhook URLs as secrets. Never place a production webhook in public documentation or Git.

## Troubleshooting
### E does nothing
Confirm you are inside the configured interaction area, the duty resource is running, and another resource has not taken over the same control in a way that prevents the interaction.

### `/dutysetup` is denied
That is expected for users without setup permission. Check the version-specific setup ACE/group.

### Department does not appear
Check the internal identifier and syntax. One character of difference between department configurations can break suite integration.

### Duty works but headtag/chat does not change
Troubleshoot the integration boundary: verify all components use the same department identifier and that each individual resource is running.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
