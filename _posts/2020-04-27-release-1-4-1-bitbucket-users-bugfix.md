---
layout: post
title:  "SCM Backup 1.4.1 released: Backing up users (not teams) from Bitbucket was broken"
author: cs
date:   2020-04-27 22:00:00 +0100
tags:
- release
---

[SCM Backup 1.4.1](https://github.com/christianspecht/scm-backup/releases/tag/1.4.1) is available to download.

There is only one change:

- [Backing up repositories owned by a user from Bitbucket is working again](https://github.com/christianspecht/scm-backup/issues/52) (repositories owned by teams were not affected).

--- 

What happened?  
Last year, Bitbucket made some breaking changes in their API because of GDPR, and I [had to release a bugfix version]({% post_url 2019-04-16-release-1-2-1-bitbucket-api-breaking-changes %}) where I changed the API calls for getting a list of a user's repos.

The solution worked fine until a few days ago, when the API call I added last year started returning 404s.

I contacted Bitbucket support, and according to their answer, that API call should have been deprecated last year as well, but accidentally was left working. Now they noticed it and removed it, and advised me to use a different call.
