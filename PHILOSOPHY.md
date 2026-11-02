# Philosophy

This project adapts the [superpowers](https://github.com/obra/superpowers) idea — ship an
engineering culture as plain markdown instead of code — to the specific constraints of a
hackathon: a fixed deadline, a vague prompt, and a demo at the end instead of a production
system.

Three things change relative to normal "superpowers"-style engineering:

1. **Lightweight verification, not test suites.** No TDD, no two-pass code review — but every
   piece still gets a concrete, explicitly-defined check before it's considered done. The golden
   path and each added feature are built and verified in a loop, one piece at a time, instead of
   one big build followed by one big QA pass at the end.
2. **Scope control is the main skill.** Most hackathon failure isn't bad code, it's never
   finishing a demoable slice because scope kept growing. Every phase exists to force a scope
   decision before more building happens.
3. **A decision log is a deliverable, not a nice-to-have.** Especially for recruiting-linked
   hackathons, "what did you decide and why" is often judged as heavily as the product. Both
   modes keep a running log; guided mode makes the user author the log's reasoning instead of
   the agent.
4. **Problem definition and verification are where human judgment matters most.** Everything in
   between (scoping mechanics, stack choice, polish) can run on sensible defaults; what the
   problem actually is, and what counts as "correct," are the two calls that most need a human
   who'll have to stand behind the answer later.

## The two modes

- **[hackathon-guided](skills/hackathon-guided/SKILL.md)** — for hackathons where your personal
  involvement in key decisions is part of what's being evaluated (recruiting-linked events,
  anything you'll need to defend in an interview). The agent stops at every decision point listed
  in each phase file and makes the user choose.
- **[hackathon-speed](skills/hackathon-speed/SKILL.md)** — for hackathons judged purely on the
  output. The agent decides at each decision point using the stated defaults, logs the choice,
  and keeps moving. It only stops when genuinely blocked (missing credentials, ambiguous prompt,
  conflicting constraints).

Both modes share the same phases, defined once in [phases/](phases/) so the two modes never
drift apart on *what* to do — only on *who* decides. The one exception is Phase 0: time budget,
team composition, and the real deadline are inputs the agent can't invent, so Phase 0 is always
settled with the user, in guided *and* speed mode alike.

## Phases

0. [Kickoff & Guardrails](phases/00-kickoff.md)
1. [Problem Clarification](phases/01-problem-clarification.md)
2. [MVP Scoping](phases/02-mvp-scoping.md)
3. [Stack Lock-in](phases/03-stack-lockin.md)
4. [Build & Verify Loop](phases/04-build-verify-loop.md)
5. [Demo Polish](phases/05-demo-polish.md)
6. [Pitch Prep](phases/06-pitch-prep.md)

Work through them in order. Don't start the Build & Verify Loop before MVP Scoping has produced
a written scope; don't start Demo Polish before every Must-demo piece has actually been through
the loop. A fresh agent picking this up mid-hackathon should check for an existing `kickoff.md`
and the other output files before doing anything else, and resume from the first phase whose
output is missing — never silently restart at Phase 0/1 and overwrite what's already decided.

## This is a default, not a rulebook

Every phase, decision point, and rule in this repo is a sensible default — not a process to
enforce on the user over their actual wishes. Hackathons differ too much for one fixed sequence
to fit all of them: a team might already have a locked stack, want to skip straight to building,
or want to revisit a "settled" phase mid-build because something changed. When the user
explicitly says what they want to do, follow that — don't stall them on process, don't argue to
stay in-sequence, and don't treat a skipped phase as an error. Flag it (e.g. "heads up, we're
skipping MVP scoping — teams that skip it are the ones who usually run out of time with nothing
demoable, just so you know") and move on. These phases exist to be useful, not to be obeyed.
