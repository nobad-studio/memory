---
name: pr-bot-rules-approve
description: PR automation: AI reviews and comments; approvals only by fixed rules, never by AI judgment
type: decision
date: 2026-11-17
---

Maintainer chose "AI reviews, rules approve". Claude review (`claude-review.yml`) comments only; it's off until a
`CLAUDE_CODE_OAUTH_TOKEN` secret is added. A rule-based auto-merge workflow (File Bridge-only PRs, Dependabot after a
human approval) was designed but not added: writing it needs the maintainer's explicit go-ahead.

**Why:** NOBAD VPN runs as admin; a crafted PR must not be able to talk an AI into approving it.
**How to apply:** prefer GitHub's built-in auto-merge button; never give an AI or bot account approval rights.
