---
date: "2024-04-19T12:32:19+03:00"
description: |
  <https://github.com/xwmx/nb> is a command line and local web note‑taking, bookmarking, archiving, and knowledge base application
id: wadgeynunwaiaji7h0w63vc
publish: true
tags:
- source/app
title: Nb
updated: 1714121309336
---

## Setup github sync

Remote:

```bash
mkdir nb
git init --bare nb/personal.git
git init --bare nb/work.git
```

Local:

```bash
nb notebook add personal
nb notebook add work
nb personal:remote set user@domain/com:/home/user/nb/personal.git
nb work:remote set user@domain/com:/home/user/nb/work/git.
```bash
