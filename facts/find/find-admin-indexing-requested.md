---
name: find-admin-indexing-requested
description: Maintainer asked for an optional admin 'turbo' index for NOBAD Find; not built, app never runs elevated
type: open
date: 2026-11-17
---

On 2026-11-17 the maintainer asked for an optional elevated index (NTFS change journal/MFT) with reminders to
turn it on, reversing the earlier "normal user only" choice. It has not been built; NOBAD Find still never runs
elevated. A kernel driver is out (driver signing, crash risk, no accuracy gain).
