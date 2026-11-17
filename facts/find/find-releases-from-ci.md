---
name: find-releases-from-ci
description: NOBAD Find releases only from CI: find-v tag -> find-release.yml, attested, never the repo's 'latest'
type: decision
date: 2026-11-17
---

Tag `find-vX.Y.Z` on `main` -> `.github/workflows/find-release.yml` builds on a clean runner, attests the
installer and publishes the GitHub Release with `--latest=false`. Playbook: `docs/ai/playbooks/release-find.md`.
The website's `releases/find/releases.json` is filled only by its publish script from the CI build.

**Why:** same trust model as NOBAD VPN; both share the Nobad-VPN repo, and VPN links rely on its "latest" release.
**How to apply:** never `gh release create` by hand; never mark a Find release as latest.
