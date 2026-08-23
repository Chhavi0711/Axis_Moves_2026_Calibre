# 04 - Operating Model

## The core loop

Axis Calibre runs as a closed feedback loop, not a one-time reassignment of who handles
what:

**Customer Request → AI matches Track Record + Capacity → Best-Suited Person Decides → Outcome Updates the Record**

Each stage feeds the next, and the loop's own output (the outcome) becomes its next
input (an updated Calibre record) - so the system's routing quality is designed to
improve with use rather than stay static after launch.

There is a second, quieter loop running alongside it: every resolved complex case
leaves behind a short, searchable note - what was decided and why. That's the mechanism
behind the Institutional Memory Reuse KPI (see
[`05_impact_and_metrics.md`](05_impact_and_metrics.md)) - institutional judgment
compounds because it's captured as it's created, instead of leaving with departing
employees.

## Roles in the model

| Role | What changes | What stays the same |
|---|---|---|
| **Officer / RM** | Can be matched directly to cases based on track record, not just cases within their formal authority tier | Reports to the same manager, holds the same title |
| **Senior Manager / Head** | No longer the default first stop for every case in their tier - only matched when their track record is the best fit | Retains sanctioning authority within the existing framework; still makes calls matched to them |
| **AI / matching layer** | New: matches track record + capacity to a case, scores calibration, and keeps a tamper-evident record | Never approves or overrides a human decision |
| **Existing sanctioning committees** | Stop approving individual transactions case-by-case; instead audit the fairness and calibration of the system itself | Still the body accountable for sanctioning quality - the object of their review changes, not their existence |
| **Governance Committee** (new) | Owns the calibration methodology, audits case-mix fairness, hears appeals, signs off on authority-limit changes each quarter | Reports into Axis's existing risk and audit structures - not a new standalone department |

## Process flow in practice

1. A customer request enters the existing intake process (no change here - this is
   intentionally the same entry point staff and customers already use)
2. The matching layer scores the case against available employees' Calibre records and
   current capacity, and routes it to the best-suited person - who may be several
   "levels" below where the case would have gone under the title-based ladder
3. That person makes the decision, using the same sanctioning authority and compliance
   checks that already exist for their role and case type
4. The outcome (approved/declined, and how it played out) is fed back into that
   person's Calibre record, adjusting it for the next round of matching

## The Governance Committee

A specific body sits at the center of the oversight model - senior leaders plus
rotating peers, not a new standalone department. Its mandate is scoped narrowly:

- Owns and periodically reviews the calibration methodology, including what counts as
  "difficult" for a given case
- Audits case-mix fairness, so no employee is penalised for a structurally harder book
  than their peers
- Hears appeals from employees who dispute a calibration outcome
- Signs off on authority-limit changes on a quarterly cadence - AI's live score is used
  for day-to-day case routing, but an employee's actual discretionary limit only moves
  after a human governance review, which keeps the system auditable and prevents
  whiplash from a single strong or weak stretch

This scopes the Committee as an extension of a function Axis already runs - internal
audit and model risk management - rather than a new regulatory category. It reviews
calibration the way an internal audit function already reviews lending quality today.

## Governance: what does *not* change

- The RBI-compliant sanctioning framework itself, including the board-approved ceiling
  on discretionary authority for each grade - calibration can move someone up faster
  within their band, or restrict them below their nominal limit, but it can never move
  anyone past the ceiling already sanctioned for their role
- Who is legally/formally authorized to sanction a given case type or exposure size
- Named accountability - every decision still has one identified, accountable officer
  of record; nothing here diffuses responsibility to a committee or an algorithm
- Independent audit oversight - extended to cover the new scoring mechanism, not
  replaced by it

## Adoption pathway

We proposed a staged rollout specifically to avoid a "big bang" governance change,
which would be both operationally risky and a hard sell to a jury evaluating execution
feasibility:

1. **Pilot**: SME lending, 2–3 regions, run as a **dual-run** against the existing
   approval grid (both systems operate in parallel so outcomes can be compared directly,
   with no live decision depending solely on the new system yet)
2. **Expand**: extend matching to retail credit and risk officers once pilot results
   validate the mechanism; formalize governance structures based on what the pilot
   surfaces
3. **Enterprise**: make track records portable across the organization, and extend the
   mechanism beyond lending - illustratively to Fraud, Corporate Banking, Treasury,
   Collections, and Customer Disputes, i.e., any decision domain where judgment quality
   can be tracked and matched to cases

This sequencing was a deliberate response to the brief's requirement to show *how* the
operating model works in practice, not just what it would look like once fully live.
