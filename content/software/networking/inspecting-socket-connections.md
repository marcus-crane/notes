---
title: "How can I inspect socket connection states"
date: 2024-08-10
tags:
  - "software"
  - "networking"
  - "unix"
  - "sockets"
---

Often times, it can be useful to inspect the state of socket connections made by applications.

You can use the tool `ss` to inspect and even kill connections.

```console
$ ss # See a list of all sockets
$ ss -t -p # See all TCP sockets with process information
$ ss -K -t '( dport = :6514 )' # Kill all TCP connections open to destination port 6514
```