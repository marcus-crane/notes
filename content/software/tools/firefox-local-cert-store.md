---
title: "How can I use my local certificate store with Firefox?"
date: 2024-08-10
tags:
  - "browsers"
  - "enterprise"
  - "firefox"
  - "software"
---

From time to time, I have troubles with Firefox since it seems to clash with a corporate proxy we use.

Using the built-in certificate store rather than Firefox's own managed store seemed to "fix" this issue.

To do this, you'll want to navigate to `about:config` and then toggle `security.enterprise_roots.enabled` to `true`.
