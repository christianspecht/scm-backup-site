---
layout: post
title:  "SCM Backup 1.5.2 released: Bitbucket/Mercurial bugfix"
author: cs
date:   2020-08-25 22:00:00 +0100
tags:
- release
---

[SCM Backup 1.5.2](https://github.com/christianspecht/scm-backup/releases/tag/1.5.2) is available to download.

Changes:

- [Fix Bitbucket errors caused by Mercurial repos](https://github.com/christianspecht/scm-backup/issues/60)  
  *(2 months after Bitbucket's Mercurial deprecation, their API still returns Mercurial repos but cloning/pulling them fails -> ignore them)*
- [Show operating system on startup](https://github.com/christianspecht/scm-backup/issues/59)
