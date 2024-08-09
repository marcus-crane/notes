---
title: "How can I view macOS network filter rules?"
date: 2024-08-10
tags:
  - "macos"
  - "software"
  - "networking"
---

```console
sudo pfctl -s all
```

The `rdr pass` entries might be of interest.

You can then use tools like `lsof` and `pstree` to find out more ie; `lsof iUDP:53535 -n -P`

Config can be flushed with `sudo pfctl -f /etc/pf.conf`