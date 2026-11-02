# Phase 5 — Demo Polish

**Goal:** spend remaining time on what judges will actually see, not on unseen robustness.

## Steps

1. Walk the *exact* click-path that will be demoed live, start to finish, as if you were a judge
   seeing it for the first time.
2. Fix anything broken **on that path only**. A bug off the demo path that won't be shown is not
   worth fixing right now.
3. Add visual polish, seed/sample data, and realistic content only where it's on the demo path.
4. Explicitly deprioritize: edge cases, error handling for inputs you won't demo, general code
   cleanup, "while I'm in here" refactors.
5. Execute the demo-day safety plan from `kickoff.md`: git-tag the current known-good build
   before any further risky changes, and record the backup demo video/recording if that was the
   plan. Double-check the real submission deadline (incl. upload/render lead time) against time
   remaining.

## Decision point

> **How much of the remaining time budget goes to polish vs attempting one more Nice-if-time
> feature** is the decision — this is the classic hackathon trap (one more feature vs a demo
> that actually looks finished). Surface the remaining time and the options explicitly.

## Output

- A demo-ready build where the golden path (and any added Must-demo features) look finished when
  clicked through in demo order
