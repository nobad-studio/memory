---
name: auto-approve-file-bridge-prs
description: File Bridge PRs merge on green tests with no review; no AI bot ever gets approval rights
type: decision
date: 2026-11-17
---

In `nobad-studio/file-bridge` the "Protect main" ruleset needs a PR and a green `file-bridge-tests`, 0 approvals, so
the file-bridge team merges its own PRs. Workflows (`.github/`) stay with @AryanGupta-234.

**Why:** Harsh must never wait on the maintainer for his own app, but an AI approving code is a prompt-injection risk.
**How to apply:** AI reviews may comment, never approve. Approval by fixed rules only (see org/pr-bot-rules-approve).
