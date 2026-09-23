---
title: "KruigerHUD"
description: "Full KruigerHUD installation, postal setup, HUD commands, controls, customization, departments, and troubleshooting."
category: "Paid Scripts"
order: 230
keywords: "KruigerHUD configuration commands ACE permissions troubleshooting"
---

# KruigerHUD

KruigerHUD is the main in-game HUD component of the Kruiger Labs FiveM package.

## Established commands and controls

```text
/hud
/postal [code]
/togglespeed
```

The package also uses the established controls **L** and **F1** for HUD-related functionality exposed by the configured release.

## Postal map requirement
KruigerHUD's postal presentation was designed around the **Big Daddy Scripts Postal Map** referenced by the Kruiger Labs product listing. If you use another postal map, the postal data/alignment expected by the HUD may not match.

Install/start the required postal map before diagnosing postal alignment as a HUD bug.

## Installation
1. Back up your current HUD configuration.
2. Upload KruigerHUD.
3. Install/start its documented map/dependencies.
4. Disable a conflicting HUD only after confirming the replacement is configured.
5. Configure display options and departments.
6. Ensure dependencies first, then KruigerHUD.
7. Test on multiple screen resolutions.
8. Test on foot and in vehicles.
9. Test postal navigation.
10. Test user HUD settings/toggles.

## `/postal [code]`
Use a postal code from the installed supported postal map:

```text
/postal 123
```

Test several locations before launch.

## Departments
Where department-aware HUD elements are enabled, use the same internal department identifiers as Duty, Headtags and other suite components.

## Troubleshooting
### Postal points to the wrong place
Verify the postal map/resource first. A mismatched postal dataset can produce correct code behavior with incorrect world locations.

### HUD overlaps another HUD
Another HUD is still running or framework HUD elements were not disabled as required.

### HUD disappears
Check the client console/NUI errors, configuration syntax, and whether the resource restarted while a player was connected.

### Vehicle information is incorrect
Test without another vehicle HUD/speedometer modifying the same display/state.

### Looks correct at 1080p but not another resolution
Test the UI at common aspect ratios/resolutions and report the exact resolution with screenshots.
