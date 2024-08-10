---
title: "How can I perform a regex search in Powershell?"
date: 2024-08-10
tags:
  - "powershell"
---

# How can I perform a regex search?

You can check if a character contains a string by using the cmatch operator like so:

```powershell
$word = "Hello"
$word -cmatch "[A-Z]"
// True
```
