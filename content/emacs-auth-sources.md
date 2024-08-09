---
title: "How can I find out where Emacs is checking for passwords?"
date: 2024-08-09
tags:
  - "elisp"
  - "emacs"
---

You can see a list of current `auth-sources` by running the following `elisp` function

```lisp
> auth-sources
(password-store "~/.authinfo.gpg")
```
