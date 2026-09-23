---
title: "Private GitHub Repo Deployment"
description: "A practical step-by-step Kruiger Labs guide to private github repo deployment."
category: "FiveM Servers"
order: 98
keywords: "Private GitHub Repo Deployment step by step Kruiger Labs"
---

# Private GitHub Repo Deployment

This guide walks through **Private GitHub Repo Deployment** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

## Before you change anything

Confirm the repository, branch, destination folder and whether the server has terminal/SSH access. Back up local edits. Never place PATs, SSH private keys, `.env` files or production credentials in the repository.

## First-time setup

Install Git if the host supports it. Clone into the intended parent directory, inspect the resulting folder, and confirm the resource/application entry files exist. For a private repository use a narrowly scoped credential or deploy key supported by your host.

## Normal update workflow

Run `git status` first. If clean, fetch/pull the intended branch. Review the changed files, install dependencies only when lockfiles/package requirements changed, then restart only the required service/resource. Finish with a cold-boot test.

## When `git pull` refuses

Do not use `git reset --hard` until you know what would be lost. Inspect `git status` and `git diff`. Preserve intentional server-only changes, reconcile conflicts, and keep secrets outside tracked files.

## Verification

Record the commit hash deployed, confirm the application/resource reports the expected version, test its primary function, then inspect logs for errors.


## Document status

**Last reviewed:** September 2026  
**Version note:** Use the instructions that match your installed product/resource version. When behavior differs from your release, check its release notes before changing production configuration.
