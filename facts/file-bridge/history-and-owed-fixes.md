---
name: history-and-owed-fixes
description: NOBAD File Bridge by @harshRaj1601: own repo since 2026-11-17; security fixes still owed before its first release
type: open
date: 2026-11-17
---

Built by @harshRaj1601 (team `file-bridge`, Maintain), merged into Nobad-VPN on 2026-11-16 (PR #27, formerly NOBAD
Files in `apps/files/`), split into `nobad-studio/file-bridge` on 2026-11-17 with his authorship kept.

Fixed: downloads escaping the target folder (Nobad-VPN #29), sudo password on a server prompt (#32).
Owed before any release: file-bridge #4 private data folder (PR #1), #3 bundle Monaco locally (no CDN), #5 green test
suite + hardening + `uv sync --locked`. PR #2 (web UI stage 3) has failing tests.

**How to apply:** the ordered task list is in file-bridge's `AGENTS.md` ("Current work"). Don't release before #3-#5.
