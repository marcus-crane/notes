---
title: "How can I extract macOS signatures from binaries?"
date: 2024-08-10
tags:
  - "macos"
  - "codesigning"
  - "certificates"
  - "x509"
---

From time to time, it can be useful to know who signed a given macOS application.

You can do that like so:

```console
$ cd /tmp/codesign
$ codesign --display --extract-certificates $(which curl)
// This will create some files in the current directory
$ ls
codesign0 codesign1 codesign2
$ qlmanage -c public.x509-certificate -p codesign*
```

Running `qlmanage` will pop open a Finder preview window with the metadata for the attached signature