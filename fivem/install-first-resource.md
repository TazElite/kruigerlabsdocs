---
title: "Installing Your First Downloaded Resource"
description: "Safely install a third-party FiveM resource without the common nested-folder and dependency mistakes."
category: "FiveM Servers"
order: 8
keywords: "FiveM Installing Your First Downloaded Resource beginner step by step"
---

# Installing Your First Downloaded Resource

Safely install a third-party FiveM resource without the common nested-folder and dependency mistakes.

## Read first

Read the resource README/product docs before uploading. Identify dependencies, framework requirements, database migrations, config steps, resource name, and start order.

## Upload

Extract the archive locally. Upload the actual resource directory so `fxmanifest.lua` sits directly inside it.

## Configure

Back up the default config before editing. Use placeholders only until you intentionally add real credentials in private server-side locations.

## Start

Install dependencies first. Run `refresh`, then `ensure ResourceName`, and read the first relevant console error.

## Cold boot

Add it to startup configuration and fully restart the server. A resource that only works after manual restart is not fully installed.
