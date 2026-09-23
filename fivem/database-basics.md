---
title: "Database Basics"
description: "Set up MySQL/MariaDB-backed FiveM resources without exposing credentials or importing schemas blindly."
category: "FiveM Servers"
order: 65
keywords: "Database Basics FiveM step by step"
---

# Database Basics
Many frameworks and advanced resources store persistent data in MySQL/MariaDB.

## Safe setup flow
1. Create the database.
2. Create a database user with only the access it needs.
3. Store the connection information privately.
4. Install the database adapter required by your framework/resource.
5. Import only the schema/migrations supplied by the product.
6. Start the database dependency before resources that use it.
7. Watch for connection or migration errors on boot.

## Never publish credentials
A database connection string is a secret. Keep it out of public Git repositories and screenshots.

## Before importing SQL
Back up an existing database. Read the product's upgrade instructions before importing a schema into a server that already has data.

## Success check
A cold server boot connects without database errors and persistent data survives a reconnect/restart as expected.
