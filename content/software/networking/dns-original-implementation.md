---
title: "How was DNS originally implemented?"
date: 2024-08-09
tags:
  - "dns"
  - "historical"
---

Back in the day, there was just one file: `HOSTS.TXT`.

It contained a name-to-address mapping for every entity within [ARPANET](https://en.wikipedia.org/wiki/ARPANET).

`/etc/hosts` used to be compiled from `HOSTS.TXT`

It didn't scale for a number of reasons:

- As soon as administrators pulled the latest version of HOSTS.TXT, it would already be out of date
- There was no way to enforce constraints eg; no duplicates on hostnames
- It took a lot of resources to serve it up to every administrator
