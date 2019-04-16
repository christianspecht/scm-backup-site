---
layout: post
title:  "SCM Backup 1.2.1 released / Breaking changes in the Bitbucket API!"
author: cs
date:   2019-04-16 22:35:00 +0200
tags:
- release
---

[SCM Backup 1.2.1](https://github.com/christianspecht/scm-backup/releases/tag/1.2.1) is available to download.

Changes:

- [Disabled some integration tests that work on my local machine, but never return on AppVeyor](https://github.com/christianspecht/scm-backup/issues/15)
- [GitHub/Bitbucket: for backing up repos owned by users, enforce authentication with the same user](https://github.com/christianspecht/scm-backup/issues/29)
- [Bitbucket API calls now use the user's UUID](https://github.com/christianspecht/scm-backup/issues/32) *(see below)*

---

> ### Please note: Breaking changes in the Bitbucket API on April 29, 2019!
> 
> Bitbucket will implement breaking changes in its 2.0 API soon (read [the announcement](https://developer.atlassian.com/cloud/bitbucket/bitbucket-api-changes-gdpr/) and [the migration guide](https://developer.atlassian.com/cloud/bitbucket/bbc-gdpr-api-migration-guide/)).
> 
> Essentially, all API requests to [`repositories/{username}`](https://developer.atlassian.com/bitbucket/api/2/reference/resource/repositories/%7Busername%7D) *(which SCM Backup uses to get a list of the user's repos)* will require the user's UUID instead of the username, but only for **users**, not for **teams**.
> 
> **This means that if you're using an older version of SCM Backup to backup the repositories of a Bitbucket *user*, your backups will stop working on April 29, 2019.**
> 
> Unfortunately there's only one solution: Update SCM Backup to version 1.2.1 or newer.

