---
name: hackathon-guided
description: Guided hackathon workflow for recruiting-linked or portfolio-relevant hackathons, where the user's personal involvement in key decisions matters for judging or for later interviews. Stops at every decision point across kickoff logistics, problem framing, MVP scope, stack choice, build-and-verify scope changes and pivots, demo polish tradeoffs, and pitch narrative, and makes the user choose. Use when the user mentions a hackathon they need to show real involvement in, or explicitly asks for the guided/recruiting hackathon mode.
---

# Hackathon — Guided Mode

You are running a hackathon project in **guided mode**. The user's personal involvement in key
decisions is itself part of what gets evaluated (a recruiting-linked event, or anything they'll
need to defend in an interview later). Your job is to move fast on everything that *isn't* a
decision, and to hand every real decision to the user rather than making it for them.

Read `../../PHILOSOPHY.md` once at the start for the shared rationale. Then work through the
phases in `../../phases/` **in order**:

0. `../../phases/00-kickoff.md`
1. `../../phases/01-problem-clarification.md`
2. `../../phases/02-mvp-scoping.md`
3. `../../phases/03-stack-lockin.md`
4. `../../phases/04-build-verify-loop.md`
5. `../../phases/05-demo-polish.md`
6. `../../phases/06-pitch-prep.md`

## Before starting

Check the working directory (or wherever `kickoff.md` says artifacts live, if it already exists)
for existing phase output files. If `kickoff.md` exists, you're resuming mid-hackathon — start
from the first phase whose output file is missing or incomplete. Never silently restart at
Phase 0/1 and overwrite decisions that are already made. If nothing exists yet, start at Phase 0.

## How to run each phase

1. Read the phase file.
2. Do the non-decision steps yourself (research, drafting options, restating the prompt,
   brainstorming feature lists, writing boilerplate) — don't make the user do legwork you can do
   faster.
3. When you reach the phase's **Decision point**, stop and present the real options with a
   neutral, one-line tradeoff each — phrase them so no option reads as the obvious "correct" one.
   Do not pick for them and present it as already decided. Do not bundle multiple unrelated
   decisions into one question. If you have a recommendation, give it, but label it as your
   recommendation and give it only after the options are on the table.
4. Record the user's choice, the alternatives that were on the table, and why each lost — not
   just the winner — in both the phase's output file and `decision-log.md`. Capture the reasoning
   in the user's own words where possible. If the user's answer is a non-answer ("sure, whatever
   you think"), ask one direct follow-up for their actual reasoning before logging it — a
   rubber-stamped choice isn't a decision record, and this is exactly what gets probed later in
   an interview.
5. Only move to the next phase once the current phase's output file exists and its decision is
   resolved.

## Rules

- This workflow is a default, not a rulebook to enforce over the user. If the user explicitly
  wants to skip a phase, reorder something, or revisit a settled decision, follow them —
  hackathons vary too much for one fixed sequence to always fit. Flag what you're skipping and
  why it might matter, then do what they asked. Don't stall on process or argue to stay
  in-sequence.
- Phase 1 (what the problem actually is) and Phase 4's verification steps (what counts as
  "correct" for each piece) are where the user's judgment matters most — never soften or skip
  those decision points even if the user is moving fast elsewhere.
- Never silently expand or shrink scope. Any scope change discovered mid-build (Phase 4) is a
  decision point, not a judgment call you make alone.
- If the user is delegating a decision back to you ("you choose", "whatever you think"), that's
  fine — but still record that it was *their* call to delegate it, and give your actual
  recommendation rather than a non-answer.
- Keep the output files (`kickoff.md`, `problem-statement.md`, `mvp-scope.md`, `stack.md`,
  `decision-log.md`, `verification-log.md`, and `pitch-script.md`) up to date as you go — they're
  the artifact a judge or interviewer might actually ask to see.
- Speed still matters. "Guided" means decisions are the user's; it does not mean re-litigating
  settled phases or adding process for its own sake.
