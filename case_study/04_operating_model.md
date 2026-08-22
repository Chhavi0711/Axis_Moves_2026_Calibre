# 04 - Operating Model

## The core loop

Axis Calibre runs as a closed feedback loop, not a one-time reassignment of who handles
what:

**Customer Request → AI matches Track Record + Capacity → Best-Suited Person Decides → Outcome Updates the Record**

Each stage feeds the next, and the loop's own output (the outcome) becomes its next
input (an updated Calibre record) - so the system's routing quality is designed to
improve with use rather than stay static after launch.

## Roles in the model

| Role | What changes | What stays the same |
|---|---|---|
| **Officer / RM** | Can be matched directly to cases based on track record, not just cases within their formal authority tier | Reports to the same manager, holds the same title |
| **Senior Manager / Head** | No longer the default first stop for every case in their tier - only matched when their track record is the best fit | Retains sanctioning authority within the existing framework; still makes calls matched to them |
| **AI / matching layer** | New: matches track record + capacity to a case, and feeds outcomes back into records | Never approves or overrides a human decision |
| **Governance / audit function** | New oversight responsibility: independently auditing Calibre scoring for fairness and gaming resistance | Existing RBI-compliant sanctioning grid is unchanged and still the system of record for approvals |

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

## Governance: what does *not* change

- The RBI-compliant sanctioning framework itself
- Who is legally/formally authorized to sanction a given case type or exposure size
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
