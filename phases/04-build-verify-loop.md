# Phase 4 — Build & Verify Loop

**Goal:** get the golden path working *and confirmed correct*, then extend it one Must-demo
feature at a time — verifying each addition before starting the next one. Never let unverified
work pile up until the end.

"Runs without crashing" and "does the right thing" are different claims. This phase treats them
as two separate steps, repeated in a loop, rather than one big build followed by one big check.

## The loop

Repeat for the golden path first, then for each remaining Must-demo feature from
`mvp-scope.md`, in order:

1. **Build** the thinnest vertical slice for this one piece (touches every layer it needs —
   UI → backend → data → external API — not just one layer in isolation). The UI for this slice
   should be usable and reasonably tidy using the component library/template chosen in
   Phase 3 — not polished, but not an unstyled placeholder either. Deep visual polish still
   waits for Phase 5; this is about not letting every screen turn into a pile of unstyled divs
   that then all need fixing at once later. Skip test-first development; a sanity check is only
   worth adding where a silent failure would quietly kill the live demo.
2. **Define "verified"** for this piece *before* checking it: what specific input(s) should
   produce what specific output/behavior for this to count as correct? Be concrete — "it detects
   fraud" is not verifiable, "feeding it this sample transaction flags it as fraud and this one
   doesn't" is. For anything that will become a pitch claim (an accuracy number, "it handles X
   case"), also note *why* this check is representative of that claim, not just a convenient
   example — this is exactly what a technical judge or interviewer will probe.
3. **Verify** against that definition. Record the result (pass / fail / partially — note what's
   wrong) in `verification-log.md`.
4. If it fails and fixing it is cheap, fix it and re-verify before moving on. If it fails and
   fixing it is expensive, that's a decision point below — don't quietly ship it unverified or
   quietly cut it.
5. Only once the current piece is verified (or explicitly accepted as a known risk), move to the
   next piece in the loop.

## If the golden path itself is the problem

The steps above assume a single piece failing. Sometimes the issue is bigger: the chosen stack or
golden path turns out structurally broken (an API doesn't do what was assumed, latency kills the
UX, a library can't support the core flow) with real time still left. Don't keep patching a plan
that fundamentally doesn't work.

Check this against the **pivot checkpoint** set in `kickoff.md`. If elapsed time has passed that
checkpoint and the golden path still isn't working end to end, stop adding to it and raise a
pivot: loop back to Phase 2 (re-scope) or Phase 3 (re-pick the stack) instead of continuing
forward.

## Decision points

> **What counts as "verified" for each piece**, and why it's representative for any pitch claim,
> is a decision point. Propose a concrete check; don't assume the bar without confirming it's
> the right one.

> **When something fails verification and is expensive to fix**, whether to fix it now, cut the
> feature, or knowingly carry it as a flagged risk into the demo is a decision point. Don't drop
> agreed-on scope, or ship something unverified, without surfacing that tradeoff when it's found.

> **Whether to pivot** (re-scope or re-pick the stack) when the golden path itself isn't working
> past the kickoff checkpoint is a decision point — don't silently keep grinding on a broken plan
> past that threshold, and don't silently abandon it before the threshold either.

## Output

- A running build where the golden path and every added Must-demo feature have each been through
  the loop at least once
- `verification-log.md`: per piece, what "verified" meant, how it was checked, why it's
  representative where relevant, and the result
- `decision-log.md` updated with any cuts/fixes/accepted risks/pivots that came out of a failed
  check
