---
layout: post
title:  "SCM Backup 1.5.0 released: Breaking changes in the Bitbucket API again"
author: cs
date:   2020-05-08 20:00:00 +0100
tags:
- release
---

[SCM Backup 1.5.0](https://github.com/christianspecht/scm-backup/releases/tag/1.5.0) is available to download.

Changes:

- [Backing up Bitbucket workspaces is now fully supported](https://github.com/christianspecht/scm-backup/issues/50) ⇒ [Documentation](https://docs.scm-backup.org/en/1.5/config-bitbucket/#sources)  
**Note: Bitbucket will make [breaking API changes on October 14](https://developer.atlassian.com/cloud/bitbucket/bitbucket-api-teams-deprecation), which unfortunately means that backing up from Bitbucket with all SCM Backup versions < 1.5 won't work anymore!**  

- [Process exit code is set to `0` on success and `1` on failure](https://github.com/christianspecht/scm-backup/issues/53) *(thanks to [nzbart](https://github.com/nzbart) for contributing this)*  

- The subject of [the generated email](https://docs.scm-backup.org/en/1.5/output-email/) now [contains "Success" or "Failure"](https://github.com/christianspecht/scm-backup/issues/47)

