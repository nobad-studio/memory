---
name: nobad-find-scope
description: NOBAD Find: private offline file search, released (latest 0.7.0, 2026-11-18), on the website; activity timeline out of scope
type: decision
date: 2026-11-17
---

NOBAD Find (`apps/find/` in Nobad-VPN): private offline search over your own files on Windows, pywebview + HTML UI.
First release 0.6.0 on 2026-11-17, 0.6.1 and 0.6.2 on 2026-11-18 (0.6.2: "having X" queries, Enter keeps the window); 0.7.0 on 2026-11-18 (resource governor with per-app memory, job objects + watchdog, closing stops indexing unless keep_background, Indexing transparency page, quick find bar Ctrl+Alt+Space, splash, Settings pages); 0.8.0 = multilingual model tiers by hardware, with consent (spec docs/superpowers/specs/2026-11-18-find-governor-transparency-models-design.md); product page /products/find/ on the website. Out of scope: activity
timeline/usage history. Runs as the normal user. Design: `docs/ai/ideas/nobad-find.md`.

**Why:** the maintainer asked to release it and list it everywhere.
**How to apply:** treat it like NOBAD VPN for releases (see find-releases-from-ci) and site listings.
