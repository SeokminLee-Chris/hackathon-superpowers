# hackathon-superpowers

A [superpowers](https://github.com/obra/superpowers)-inspired skill set for running a hackathon
project end to end — from a raw problem prompt to a pitched demo — as a phased workflow checked
into plain markdown instead of baked into one tool.

Two modes, same phases, different question: *who decides?*

| | `hackathon-guided` | `hackathon-speed` |
|---|---|---|
| For | Recruiting-linked / portfolio hackathons where your involvement in decisions is evaluated | Hackathons judged purely on the output |
| At each decision point | Stops and asks you | Decides with a sensible default, logs it, moves on |
| Stops for | Every listed decision point | Only real blockers (missing creds, ambiguous prompt, conflicting constraints) |

See [`PHILOSOPHY.md`](PHILOSOPHY.md) for the reasoning, and [`phases/`](phases/) for what each
phase (Kickoff & Guardrails → Problem Clarification → MVP Scoping → Stack Lock-in → Build &
Verify Loop → Demo Polish → Pitch Prep) actually covers.

## Usage

This repo is content, not a packaged plugin: plain markdown with YAML frontmatter, cross-linked
by relative paths (`skills/*/SKILL.md` → `../../PHILOSOPHY.md` and `../../phases/*.md`). Clone
the whole repo and keep it intact — don't copy a single `skills/<name>` folder out on its own,
since its relative links resolve against the rest of the repo, not against wherever it lands.

```bash
git clone https://github.com/SeokminLee-Chris/hackathon-superpowers.git
```

How you turn this content into something your agent actually loads is deliberately left to that
agent/tool's own mechanism, since it varies:

- **Claude Code**: symlink (not copy) a whole clone into `~/.claude/skills/hackathon-superpowers`,
  or just open a session inside the cloned repo and ask Claude to read
  `skills/hackathon-guided/SKILL.md` (or `hackathon-speed`) and follow it.
- **Codex CLI, Cursor, Gemini CLI, or anything else**: open a session inside the cloned repo and
  point the agent at the same `SKILL.md`, or paste it into that tool's custom-instructions
  mechanism (`AGENTS.md`, a Cursor rule, etc.) — as long as the rest of the repo (`PHILOSOPHY.md`,
  `phases/`) stays reachable at the relative paths the file links to.

## License

MIT — see [`LICENSE`](LICENSE).
