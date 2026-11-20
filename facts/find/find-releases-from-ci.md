---
name: find-releases-from-ci
description: NOBAD Find releases only from CI in nobad-studio/find (find-v tag -> find-release.yml, attested); 0.8.5 and older stay in Nobad-VPN
type: decision
date: 2026-11-20
---

Tag `find-vX.Y.Z` on `main` of nobad-studio/find -> `.github/workflows/find-release.yml` builds on a clean runner,
attests the installer and publishes the GitHub Release (now the repo's latest). Playbook:
`docs/ai/playbooks/release-find.md` there. Releases 0.6.0 to 0.8.5 stay in nobad-studio/Nobad-VPN; check them with
`-R nobad-studio/Nobad-VPN`. The website's `releases/find/releases.json` is filled only by its publish script
(`--repo` picks the repo).

**Why:** same trust model as NOBAD VPN; attestations name the repo that built them, so old releases can't move.
**How to apply:** never `gh release create` by hand; never re-upload or move a published release.
