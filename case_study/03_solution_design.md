# 03 - Solution Design: Axis Calibre

## The core concept

**Calibre** - how good someone's judgment turns out to be, tracked over time. It's the
single mechanism the entire proposal is built around: a continuously updated record of
each employee's decision track record, used to route future cases to whoever is best
placed to judge them.

The name and definition were chosen deliberately: "Calibre" reads as a quality-of-
judgment concept, not a scoring or surveillance system - an important framing choice
given how sensitive employee-tracking mechanisms can be inside a large regulated
organization.

## Design principle: authority follows judgment, not designation

Where today's model fixes authority to a title (Officer → Senior Manager → Head, in a
strict ladder), Calibre keeps titles and compensation exactly as they are, but decouples
*routing* from that ladder. A 3-year Officer with a strong track record can be matched
directly to a case a 12-year veteran would otherwise have first claim on - because the
system is asking "who has proven the best judgment on cases like this," not "who holds
the senior title."

## Design principle: AI recommends and routes - it never decides

This is the load-bearing constraint of the whole design. AI's role is limited to two
things:

1. Matching a new case against **track record + current capacity** to identify the
   best-suited person
2. Feeding the outcome of each decision back into that person's record

A human still makes every decision, and every decision still passes through Axis's
existing RBI-compliant sanctioning framework. We treated this as non-negotiable, both
because it's the only way the idea clears a regulated-banking bar, and because it keeps
the human accountable for the call - AI shortens the *path* to a decision, not the
*deliberation* itself.

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

## What we deliberately kept simple for this round

Per the brief's own instruction to prioritize clarity over density in a 2-slide format,
we did not attempt to specify the underlying AI matching algorithm, the exact data
schema for a Calibre score, or a full audit methodology in this round's deliverable -
those sit at the level of detail we'd expect to develop in a Round 4 "Detailed PPT" or
pilot design phase, not a Board-level big-bet pitch.
