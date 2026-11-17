---
name: pre-1-5-releases-mutable
description: Releases before 1.5.0 aren't immutable (the setting only covers new releases)
type: open
date: 2026-11-16
---

Releases before 1.5.0 aren't immutable (the setting only covers new releases); anyone with write access could replace their files. Users should verify with the strict `gh attestation verify ... --signer-workflow ... --source-ref ...` command (docs/RELEASE-PROCESS.md). Optional hardening: a protected `release` environment with the owner as required reviewer on the publish job.
