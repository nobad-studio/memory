---
name: shared-memory-system
description: How every contributor's AI assistant shares memory: this repo, loaded by index, written by reviewed PR
type: decision
date: 2026-11-17
---

`nobad-studio/memory` holds one fact per file and a generated `INDEX.md`. Assistants load only the index at session
start (Claude Code: SessionStart hook in each repo; others: AGENTS.md) and open a fact only when relevant, to save
tokens. New facts arrive as PRs, checked by `tools/mem.py check` and reviewed by code owners.

**Why:** one memory across repos, people and AI tools; reviewed because every assistant trusts what it loads.
**How to apply:** record decisions here, not in chat or private notes. Run `python tools/mem.py status` to see who is
working on what before starting.
