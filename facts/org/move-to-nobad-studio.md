---
name: move-to-nobad-studio
description: Where each NOBAD product lives after the 2026-11-17 move to the nobad-studio organization, and what's left
type: open
date: 2026-11-17
---

Repos: `Nobad-VPN` (NOBAD VPN + NOBAD Find; renamed from `nobad`, transferred from AryanGupta-234/Nobad, old URLs
redirect), `website` (Cloudflare Workers Builds deploys `nobad-platform` from its `main`), `file-bridge` (split with full
history), `.github` (org profile), `memory` (this). Site: https://nobad-platform.nobad-studio.workers.dev/ (the old
`aassworld99` address is dead). Attestation checks must name the exact repo (`-R nobad-studio/Nobad-VPN`).

Left: remove the duplicate `site-pages/`, `releases/`, `assets/`, `scripts/`, `package.json`, `wrangler.jsonc` and
`apps/file-bridge/` from Nobad-VPN (maintainer said "not yet": ask first).

**How to apply:** edit the site in `website`, File Bridge in `file-bridge`; never in Nobad-VPN's leftover copies.
