# Phase 3 — Stack Lock-in

**Goal:** pick technology fast without skipping a real choice. A stack discussion that runs past
15 minutes is itself a scope failure — but picking from zero alternatives isn't a decision
either.

## Steps

1. List hard constraints: required/bonus sponsor APIs, team's existing familiarity, deployment
   target (must it be a deployed URL? a local demo is fine?), anything the rules forbid.
2. Propose **three** candidate stacks — not one, and not an open-ended menu — each with a
   one-line tradeoff, all evaluated primarily on "fastest path to the golden path running end to
   end." Keep it fast: three concrete options to react to, not a drawn-out architecture debate.
3. Each candidate's stack includes a **UI approach**, not just backend/data — a component
   library, template, or design kit that gets to decent-looking screens fast (judges see the UI
   before they see the code). "This will look rough and we'll fix it later" is a red flag in any
   candidate, not an acceptable plan.
4. If a sponsor technology or prize track is worth targeting deliberately (even if it's not the
   fastest choice), make sure at least one candidate reflects that, and call out the tradeoff
   explicitly rather than burying it.
5. Confirm nobody on the team is being asked to use something they've never touched under time
   pressure, unless that's a deliberate, acknowledged risk.

## Decision point

> **Which of the three candidates to go with** — and in particular any case where "fastest" and
> "best for a prize track/sponsor bonus" disagree — is the decision. Present the tradeoffs
> neutrally; don't phrase them so one option is obviously "correct."

## Output

`stack.md`:
- Chosen stack, one line of why per major piece
- The two alternatives that were considered and why they lost
- UI approach chosen and why
- Any sponsor/prize tradeoffs taken on purpose
- Deployment plan (where does the demo actually run from)
