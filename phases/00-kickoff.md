# Phase 0 — Kickoff & Guardrails

**Goal:** establish the hard constraints and process guardrails that shape every later phase,
before any problem framing starts. These are facts and process calls the agent has no basis to
invent — they come from the user, in both modes.

## Steps

1. Ask for: total time budget available (e.g. "36 hours"), the *real* deadline — including
   submission-platform lead time (video render/upload time, a Devpost post deadline that's
   earlier than the "stop coding" time, etc.) — and team composition (solo, or team size with
   each member's rough skills/role leaning).
2. Ask where the working artifacts for this hackathon (`problem-statement.md`, `mvp-scope.md`,
   `stack.md`, `decision-log.md`, `verification-log.md`, `pitch-script.md`) should live — the
   project repo's root, a `docs/` folder, wherever makes sense. Once set, every later phase
   writes there.
3. Propose a rough time-budget split across Phases 1–6 based on the total available, and a
   **pivot checkpoint**: an elapsed-time/percentage threshold at which, if the golden path isn't
   working end to end yet, the team stops pushing forward and loops back to Phase 2/3 to re-scope
   instead of continuing to build on a plan that isn't working.
4. If it's a team, sketch rough role ownership (who leans frontend/backend/design/pitch). This
   gets refined once Phase 2 produces the actual feature list — don't over-finalize it here.
5. Note demo-day safety basics: when a known-good build gets git-tagged as a fallback, whether a
   backup demo recording will be made, and the actual submission deadline vs. the "stop building"
   time.

## Decision point

> **All of the above** — time-budget split, pivot checkpoint threshold, artifact location, role
> sketch, safety plan — is decided together with the user here, in *both* guided and speed mode.
> These aren't quality judgment calls with a sensible default; they're inputs the agent cannot
> know on its own.

## Output

`kickoff.md`:
- Total time budget and real deadline (incl. submission lead time)
- Team composition and rough role sketch
- Where artifacts live for the rest of the process
- Phase time-budget table
- Pivot checkpoint definition
- Demo-day safety plan

Also create `decision-log.md` in the same location. From here on, every phase appends an entry
to it (what was decided, the alternatives that were on the table, and why — see each phase's
"How to run each phase" instructions) rather than each phase keeping its own separate log.
