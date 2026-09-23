---
title: "Deploying From GitLab"
description: "A practical step-by-step Kruiger Labs guide to deploying from gitlab."
category: "FiveM Servers"
order: 99
keywords: "Deploying From GitLab step by step Kruiger Labs"
---

# Deploying From GitLab

This guide walks through **Deploying From GitLab** from preparation through verification, with a rollback path and the checks that matter in a real fivem servers environment.

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
