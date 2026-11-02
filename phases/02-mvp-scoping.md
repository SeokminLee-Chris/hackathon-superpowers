# Phase 2 — MVP Scoping

**Goal:** split the full idea into "demoable in the time available" vs "everything else," before
writing any code.

## Steps

1. Brainstorm the full feature list implied by the chosen framing from Phase 1 — don't
   self-censor yet.
2. Tag every feature:
   - **Must-demo** — without this, there is no demo.
   - **Nice-if-time** — adds polish or depth but the demo survives without it.
   - **Cut** — explicitly out of scope for this event.
3. Design one **golden path**: a single, specific end-to-end user flow (e.g. "user uploads a
   receipt photo → app extracts line items → app flags the one that looks wrong") that uses only
   Must-demo features. This is what will actually be built first and demoed live.
4. Sanity-check the golden path against the time-budget table from `kickoff.md`. If it doesn't
   fit, cut features, not corners on the remaining ones.
5. If it's a team, turn `kickoff.md`'s rough role sketch into actual ownership per Must-demo
   feature now that the real feature list exists.

## Decision point

> **The Must-demo/Cut line, and the golden path itself**, are the decision. Present the proposed
> golden path and the Cut list plainly — cutting a feature someone was excited about is exactly
> the kind of call that should not be made silently.

## Output

`mvp-scope.md`:
- Full feature list with tags
- The golden path, written as a numbered user flow
- What was cut and why
- Feature ownership per team member, if applicable
