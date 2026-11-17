# NOBAD shared memory

Decisions, open items and ideas for every NOBAD product, in one place that people and their AI assistants share.
Software with a point of view.

- **[INDEX.md](INDEX.md)**: one line per fact. Start here.
- **[facts/](facts/)**: one short Markdown file per fact, grouped by `org`, `vpn`, `find`, `file-bridge`, `website`.
- **[AGENTS.md](AGENTS.md)**: how assistants read and write it. **[skills/](skills/)**: the Claude Code skill.
- **[tools/mem.py](tools/mem.py)**: `index`, `check`, `new`, `status` (Python standard library only).

To add or change a fact: open a pull request (see AGENTS.md). CI checks the format, size and that nothing looks like a
secret; code owners review. This repository is public: never put keys, configs or personal data here.

## Hook it into a repository
Each NOBAD repo loads the index at the start of every Claude Code session through `.claude/settings.json`:

```json
{ "hooks": { "SessionStart": [ { "hooks": [ { "type": "command",
  "command": "gh api -H \"Accept: application/vnd.github.raw\" repos/nobad-studio/memory/contents/INDEX.md || curl -fsS https://raw.githubusercontent.com/nobad-studio/memory/main/INDEX.md || echo \"(NOBAD shared memory unavailable offline)\"" } ] } ] } }
```

and its `AGENTS.md` points other assistants here. The hook only reads a public file; it runs nothing from this repo.
