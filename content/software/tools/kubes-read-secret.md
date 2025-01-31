---
title: "How can I read a Kubernetes secret?"
date: 2024-08-10
tags:
  - "credentials"
  - "kubernetes"
  - "security"
---

Often times, it can be useful to check the value of a Kubernetes secret, to check that it lines up with what an application is receiving. An example might be a randomly generated secret that is shared between multiple Kubernetes resources.

Let's have a look at a mock secret:

```bash
> kubectl describe secret dummy-secret
Name:         dummy-secret
Namespace:    sports
Labels:       app.kubernetes.io/managed-by=Helm
Annotations:  meta.helm.sh/release-name: sports
              meta.helm.sh/release-namespace: sports

Type:  Opaque

Data
====
MY_FAVOURITE_FRUIT:  12 bytes
```

So here we have a secret called `dummy-secret` and one of the values within it has the name `MY_FAVOURITE_FRUIT`.

We can fetch it like so:

```bash
> kubectl get secret dummy-secret -o jsonpath="{.data.MY_FAVOURITE_FRUIT}" | base64 --decode
strawberries
```
