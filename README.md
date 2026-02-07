# Shaping Skills

Credits: inspired by Ryan Singer’s thread, [Shaping 0-1 with Claude Code](https://x.com/rjs/status/2020184079350563263).

[Codex](https://openai.com/codex/) skills for shaping and breadboarding — the methodology from [Shape Up](https://basecamp.com/shapeup) adapted for working with an LLM.

**Case study:** [Shaping 0-1 with Claude Code](https://x.com/rjs/status/2020184079350563263) walks through the full process of building a project from scratch using these skills. The source for that project is at [rjs/tick](https://github.com/rjs/tick).

## Skills

**`$shaping`** — Iterate on both the problem (requirements) and solution (shapes) before committing to implementation. Separates what you need from how you might build it, with fit checks to see what's solved and what isn't.

**`$breadboarding`** — Map a system into UI affordances, code affordances, and wiring. Shows what users can do and how it works underneath — in one view. Good for slicing into vertical scopes.

## Install

```bash
# Clone the repo, then symlink each skill into your Codex skills directory
git clone https://github.com/rjs/shaping-skills.git ~/.local/share/shaping-skills
mkdir -p "$CODEX_HOME/skills"
ln -s ~/.local/share/shaping-skills/breadboarding "$CODEX_HOME/skills/breadboarding"
ln -s ~/.local/share/shaping-skills/shaping "$CODEX_HOME/skills/shaping"
```

Each skill must be a direct child of `$CODEX_HOME/skills/` so Codex can discover it. Symlinks keep them updatable with `git pull`.

---

This README was adapted for [Codex](https://openai.com/codex/).
