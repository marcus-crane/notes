---
title: "How can I compile Emacs from source?"
date: 2024-08-10
tags:
  - "emacs"
---

The following should roughly do it. Your mileage may vary!

```shell
git clone -b emacs-27 git://git.sv.gnu.org/emacs.git
cd emacs
sudo apt-get build-dep emacs
./autogen.sh
./configure --with-x-toolkit=lucid --with-mailutils
make -j4
./src/emacs // test that its working
sudo make install
```
