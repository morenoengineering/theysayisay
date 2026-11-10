# They Say / I Say skills for Claude Code

Three Claude Code skills for technical reading, summarizing, and writing, based on the moves in *They Say / I Say* (Graff & Birkenstein):

- `technical-reading`: read a text for what it responds to, what it claims, objections, and so-what.
- `technical-summary`: faithful summaries, precise verbs, clear voices, quotes with context before and explanation after.
- `technical-writing`: they-say/I-say structure, naysayer, so-what, calibrated claims, connected prose.

## Install

The skills follow the [Agent Skills](https://agentskills.io) standard and live in `.agents/skills/`. `.claude/skills` is a symlink to it, so Claude Code sees the same files.

| Harness | Global (all projects) | Per project |
|---|---|---|
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| OpenCode | `~/.agents/skills/` (or `~/.config/opencode/skills/`, `~/.claude/skills/`) | `.agents/skills/` or `.opencode/skills/` |
| Codex CLI, other Agent Skills harnesses | `~/.agents/skills/` | `.agents/skills/` |

Install globally for every harness at once:

```sh
git clone git@github.com:morenoengineering/theysayisay.git ~/src/theysayisay
mkdir -p ~/.agents/skills ~/.claude/skills
for s in ~/src/theysayisay/.agents/skills/*/; do
  ln -sfn "$s" ~/.agents/skills/
  ln -sfn "$s" ~/.claude/skills/
done
```

`git pull` in the clone updates every harness. On Windows, or if your harness skips symlinks, copy the folders instead.
