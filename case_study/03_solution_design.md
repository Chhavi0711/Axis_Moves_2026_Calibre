# 03 - Solution Design: Axis Calibre

## The core concept

**Calibre** - how good someone's judgment turns out to be, tracked over time. It's the
single mechanism the entire proposal is built around: a continuously updated record of
each employee's decision track record, used to route future cases to whoever is best
placed to judge them.

The name and definition were chosen deliberately: "Calibre" reads as a quality-of-
judgment concept, not a scoring or surveillance system - an important framing choice
given how sensitive employee-tracking mechanisms can be inside a large regulated
organization. The name carries a deliberate double meaning: caliber, the highest
standard of judgment, and calibrated, the actual scoring mechanic behind the system -
one word doing the work of two, without needing a separate explanation for either.

## Design principle: authority follows judgment, not designation

Where today's model fixes authority to a title (Officer → Senior Manager → Head, in a
strict ladder), Calibre keeps titles and compensation exactly as they are, but decouples
*routing* from that ladder. A 3-year Officer with a strong track record can be matched
directly to a case a 12-year veteran would otherwise have first claim on - because the
system is asking "who has proven the best judgment on cases like this," not "who holds
the senior title."

## Design principle: AI recommends and routes - it never decides

This is the load-bearing constraint of the whole design. AI's role is strictly
administrative, and limited to three functions:

1. **Match and route** - pairing a new case against track record, case difficulty, and
   current capacity to identify the best-suited person
2. **Score calibration** - comparing each decision's predicted outcome against its
   actual outcome, difficulty-adjusted, to keep the track record current
3. **Keep the record honest** - maintaining a tamper-evident log of every relevant
   decision, so the record itself can't be quietly edited after the fact

A human still makes every decision, and every decision still passes through Axis's
existing RBI-compliant sanctioning framework. We treated this as non-negotiable, both
because it's the only way the idea clears a regulated-banking bar, and because it keeps
the human accountable for the call - AI shortens the *path* to a decision, not the
*deliberation* itself. Keeping AI's role strictly administrative also matters
regulatorily: algorithmic credit-decisioning draws far stricter fair-lending and
model-risk scrutiny than a routing and record-keeping layer does, and a human stays the
decision-maker of record on every case.

## Design principle: nothing about pay or title changes

We were deliberate about this because it's the single biggest lever against
organizational resistance. Calibre changes who a case is routed to. It does not change
what someone is paid, what their title is, or the formal promotion track. This keeps the
proposal inside existing HR and compensation frameworks, so it doesn't require
renegotiating the Bank's broader people systems just to pilot the idea.

## Design principle: governance and fairness are independently audited

Because Calibre scores influence routing (and, over time, visibility and reputation
inside the Bank), we built in independent auditing of the scoring mechanism itself -
both for governance/regulatory soundness and for fairness (so the system can't quietly
disadvantage certain roles, tenures, or case types). This connects directly to the
gaming risk addressed in
[`06_risks_and_rollout.md`](06_risks_and_rollout.md).

## Why this is hard to copy

Every plausible competing pitch in a challenge like this bets on better technology -
a scoring engine, a platform, a personalization layer. By 2035 every bank will have
something comparable; it becomes infrastructure, not advantage, the way electricity is
always present but never the product. Axis Calibre bets on something no competitor can
buy off the shelf: a workforce whose authority is provably, continuously earned, and a
compounding record of judgment that only gets more valuable the longer it runs. A
competitor starting this a year later starts a year behind on the one asset that
compounds - that's a structurally different kind of advantage than a faster algorithm.

For the full mechanics behind how the track record is actually calculated - difficulty
tiering, the recency-weighted scoring window, and the minimum-sample threshold before
authority moves - see [`07_calibration_mechanics.md`](07_calibration_mechanics.md).

## What we kept off the two-slide deck, and why

Per the brief's own instruction to prioritize clarity over density in a 2-slide format,
the submitted deck itself doesn't spell out the underlying matching algorithm, the
exact Calibre-score mechanics, or a full audit methodology - a Board-level big-bet pitch
isn't the place for that level of density. We worked this detail out anyway, as
preparation for the questions a sharp jury would actually ask, and it's captured in
[`07_calibration_mechanics.md`](07_calibration_mechanics.md) and in the team's own prep
materials under [`/docs/prep_materials`](../docs/prep_materials/), rather than left
unresolved.
