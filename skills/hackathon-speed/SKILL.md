---
name: hackathon-speed
description: Fast, autonomous hackathon workflow for events judged purely on the output, not on the builder's individual decisions. Works through the same phases as hackathon-guided (kickoff, problem framing, MVP scope, stack, build-and-verify, demo polish, pitch) but decides at each point using sensible defaults, logs the choice, and keeps moving. Only stops when genuinely blocked, or at the kickoff facts no agent should default. Use when the user wants maximum speed and isn't required to show personal involvement in each decision.
---

# Hackathon — Speed Mode

You are running a hackathon project in **speed mode**. Nobody is grading how involved the user
was in each call — the output is what's judged. Your job is to move through all phases with
minimal back-and-forth, deciding things yourself and telling the user what you decided, not
asking permission for each one (except Phase 0 — see below).

Read `../../PHILOSOPHY.md` once at the start. Then work through the phases in `../../phases/`
**in order**:

0. `../../phases/00-kickoff.md`
1. `../../phases/01-problem-clarification.md`
2. `../../phases/02-mvp-scoping.md`
3. `../../phases/03-stack-lockin.md`
4. `../../phases/04-build-verify-loop.md`
5. `../../phases/05-demo-polish.md`
6. `../../phases/06-pitch-prep.md`

## Before starting

Check the working directory (or wherever `kickoff.md` says artifacts live, if it already exists)
for existing phase output files. If `kickoff.md` exists, resume from the first phase whose
output is missing rather than restarting at Phase 0/1. Phase 0 itself always runs with the user
regardless of mode — time budget, team, and deadline aren't things to default.

## How to run each phase

1. Read the phase file.
2. Do every step yourself, including what the phase file marks as a "Decision point" — pick the
   option that most directly maximizes "working, demoable product within the time budget."
   Prefer the familiar/boring choice over the impressive/risky one unless the prompt's judging
   criteria explicitly reward the risky one. **Exception: Phase 0's decision point is always the
   user's** — time budget, team, and deadline aren't facts you can default your way to.
3. Still write the phase's output file and log the decision + a one-line reason — a fast decision
   is not the same as an undocumented one, and the log doubles as your own working notes across a
   long build.
4. Give the user a short status update after each phase (what was decided, what's next) rather
   than a question. Move on without waiting for acknowledgment unless you're genuinely blocked.

## When to actually stop and ask

Only interrupt the flow for things sensible defaults can't resolve:
- Missing credentials/API keys you can't obtain yourself.
- A prompt that's ambiguous in a way that changes what gets built, not just how.
- Two constraints that directly conflict (e.g. a required sponsor API that can't support the
  golden path as scoped).

Everything else: decide, log it, keep building.

## Rules

- This workflow is a default, not a rulebook to enforce over the user. If the user explicitly
  wants to skip a phase, reorder something, or revisit a settled decision, follow them —
  hackathons vary too much for one fixed sequence to always fit. Flag what you're skipping and
  why it might matter, then do what they asked.
- Don't pad the process with questions that `hackathon-guided` would ask but speed mode doesn't
  need — the whole point of this mode is fewer checkpoints.
- Don't skip phases to save time; skip *questions*, not *thinking*. A missed MVP-scoping pass is
  the single most common reason hackathon teams run out of time with nothing demoable.
