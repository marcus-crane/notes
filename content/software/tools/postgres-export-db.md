---
title: "How can I export a Postgres database?"
date: 2024-08-10
tags:
  - "databases"
  - "postgres"
---

Using `pg_dump`, which ships with the `psql` executable, it's a pretty simple progress

```bash
pg_dump --dbname={{DBNAME}} --host={{HOST}} --port={{PORT}} --username={{USERNAME}} --password --format=c > {{NAME}}.dump
# The c in --format=c stands for custom
```
