---
title: "Installing Add-on Vehicles"
description: "A practical step-by-step Kruiger Labs guide to installing add-on vehicles."
category: "FiveM Servers"
order: 117
keywords: "Installing Add-on Vehicles step by step Kruiger Labs"
---

# Installing Add-on Vehicles

This guide walks through **Installing Add-on Vehicles** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## Inspect the download

Extract it locally and identify the real resource root (`fxmanifest.lua`). Read its install notes and dependencies before uploading. Keep a backup of any resource it replaces.

## Install

Place the resource under a logical bracket folder such as `[vehicles]`, `[maps]`, `[eup]` or `[scripts]`. Preserve the expected folder name unless the author says renaming is safe.

## Manifest and data files

Check that streamed files and any required data/meta files are declared correctly by the supplied manifest. Do not invent manifest entries when the resource already ships a working manifest.

## Start and test

Run `refresh`, then `ensure ResourceName`. Read the console before joining. Test the asset in multiple relevant locations/vehicles/outfits and then cold boot the whole server.

## Typical failures

Missing assets often mean a nested folder, bad path/case, missing dependency, incorrect manifest/data declaration, or a conflict with another resource providing the same content.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
