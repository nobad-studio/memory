---
name: find-photo-model-siglip
description: NOBAD Find photo meaning uses SigLIP base (Apache-2.0, ~211 MB optional download), not OpenAI CLIP
type: decision
date: 2026-11-17
---

The maintainer approved an optional image model for finding photos by what's in them. Chosen: SigLIP base
(Google, Apache-2.0, ONNX by Xenova, pinned revision + SHA-256), off until the user allows the download.

**Why:** OpenAI CLIP's model card rules out deployed use; a permissive licence is safer to ship.
**How to apply:** keep model licences permissive; new models need a setting and the README privacy section.
