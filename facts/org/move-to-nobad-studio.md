---
name: move-to-nobad-studio
description: Where each NOBAD product lives (one repository per product since 2026-11-20), and what's left
type: open
date: 2026-11-20
---

Repos: `Nobad-VPN` (NOBAD VPN; renamed from `nobad`, transferred from AryanGupta-234/Nobad, old URLs redirect; keeps
the find-v0.6.0..0.8.5 releases), `find` (NOBAD Find, split with its history on 2026-11-20), `file-bridge` (split
with full history), `website` (Cloudflare Workers Builds deploys `nobad-platform` from its `main`), `.github` (org
profile), `memory` (this). Maintainer decision 2026-11-20: every product has its own repository. Site:
https://nobad-platform.nobad-studio.workers.dev/. Attestation checks must name the exact repo.

Left: remove the duplicate `site-pages/`, `releases/`, `assets/`, `scripts/`, `package.json` and `wrangler.jsonc`
from Nobad-VPN (its `site-build` check still builds them; maintainer said "not yet": ask first).

**How to apply:** edit the site in `website`, Find in `find`, File Bridge in `file-bridge`; never in leftover copies.
