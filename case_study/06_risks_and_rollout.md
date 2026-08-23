# 06 - Risks and Rollout

## Risks we named up front, and why

We treated risk identification as part of the pitch itself, not an appendix - a jury
evaluating "Operating Model & Execution Feasibility" is implicitly asking "what breaks
this, and have you thought about it," so we built five risks into the core proposal
rather than waiting to be asked. Two of these five (gaming and regulatory fit) are the
ones we expected to get pressed on hardest, so we prepared the deepest answers for them.

### Risk 1 - Gaming the system

**The concern:** if Calibre scores influence who gets matched to (and eventually,
implicitly, who looks good), employees have an incentive to cherry-pick easy, low-risk
cases to keep their score high, rather than take on harder judgment calls.

**Our mitigation:** we built the anti-gaming logic into the mechanism itself, rather
than bolting it on as a policy. Six things close off the incentive to game it:

- **Difficulty-adjustment** - an easy case scored against an easy-case benchmark
  doesn't move the needle, so cherry-picking doesn't pay
- **No self-selection** - employees don't request cases; the AI matcher assigns them
  based on track record and capacity, so nobody can quietly steer easy work to
  themselves
- **Mandatory case-mix diversity monitoring** - if someone's queue drifts too easy,
  it flags for Governance Committee review rather than silently continuing
- **Outcome lag** - a decision only counts toward the score once its outcome is
  actually observable (real repayment behaviour, not just "the loan was disbursed"),
  which kills the incentive to rack up unproven short-term wins
- **Blind audit sampling** - each quarter, the Governance Committee randomly pulls a
  sample of resolved cases for peer review, independent of the automated score, to
  catch subtler manipulation a purely statistical system might miss
- **Transparency as a deterrent** - the ledger and calibration methodology are visible
  to peers and audited by the Committee, closer to an open-book system than a black
  box, which is structurally harder to quietly game

The honest caveat: no scoring system is un-gameable in theory. What we can defend is
that every gaming strategy we could think of is specifically closed off by one of the
mechanisms above, and the quarterly audit exists precisely to catch what we didn't
think of. Full mechanics behind the scoring itself are in
[`07_calibration_mechanics.md`](07_calibration_mechanics.md).

### Risk 2 - Regulatory fit

**The concern:** any change to how lending/credit decisions get made in a bank has to
survive RBI compliance scrutiny - a proposal that quietly bypasses or thins out existing
checks would fail regardless of how elegant the routing logic is.

**Our mitigation:** we designed the entire mechanism to sit *inside* Axis's existing
RBI-compliant sanctioning framework from day one, rather than proposing a parallel or
replacement framework. AI's role is capped at recommend-and-route specifically so that
sanctioning authority, and the compliance checks tied to it, are untouched.

### Risk 3 - Organizational resistance

**The concern:** any system that changes who gets matched to high-visibility decisions
can trigger resistance from staff who read it as a threat to their standing, especially
senior staff whose case volume might shift under the new routing logic.

**Our mitigation:** pay and titles are explicitly untouched. This was a deliberate design
choice, not an afterthought - the proposal changes *routing*, not compensation,
hierarchy, or formal authority. Framing it this way was also meant to make the pitch
itself land better with a jury that includes senior Axis leadership: it's a change to
where cases go, not a threat to who holds a title.

### Risk 4 - A well-calibrated employee still causing a large loss

**The concern:** even someone with a genuinely strong track record can still make a
call that goes badly - a good process doesn't guarantee a good outcome every time, and
the model shouldn't be sold as if it does.

**Our mitigation:** hard, board-approved risk-weighted ceilings exist independently of
track record. Calibration only expands or restricts discretion *within* those ceilings
- it never removes them. However strong someone's calibration score, they can never be
routed a case that exceeds the ceiling already sanctioned for their grade.

### Risk 5 - The system quietly drifting back to seniority-as-usual

**The concern:** over time, informal habits or soft pressure could nudge routing back
toward "give it to the senior person anyway," quietly hollowing out the whole premise
without any single decision that looks like a reversal.

**Our mitigation:** the Governance Committee holds a standing, published audit of
whether Rising Talent Rate is genuinely shifting toward merit over time, making drift
visible and correctable rather than something that only shows up once it's already
entrenched.

## Rollout, in more detail

We proposed a three-stage rollout, each stage designed to de-risk the next:

**Stage 1 - Pilot.** SME lending, 2–3 regions, run as a dual-run against the existing
approval grid. Chosen because SME lending cases are frequent enough to generate a
meaningful comparison sample within a pilot window, and contained enough in scope to
audit closely.

**Stage 2 - Expand.** Extend matching to retail credit and risk officers, and formalize
the governance structures (audit cadence, escalation paths, fairness review) based on
what the pilot actually surfaces - rather than fully specifying governance up front,
before there's pilot evidence to design it against.

**Stage 3 - Enterprise.** Make track records portable organization-wide, and extend the
underlying mechanism beyond lending. We listed this illustratively - Fraud, Corporate
Banking, Treasury, Collections, Customer Disputes - as domains that share the same
underlying shape (a judgment call, made under some authority tier, with a traceable
outcome), without claiming any of them as validated extensions at this stage.

## What's still open

The two-slide submission deliberately doesn't spell out the exact audit methodology,
the data/privacy design for how Calibre records are stored and accessed, or a named
pilot timeline with specific regions - that level of density doesn't belong in a
Board-level big-bet pitch. We worked most of this out anyway during prep (see
[`07_calibration_mechanics.md`](07_calibration_mechanics.md) and
[`/docs/prep_materials`](../docs/prep_materials/)), but a named pilot timeline and
specific regions genuinely aren't decided yet - those are natural candidates for a
future detailed-PPT round, once/if we have that material. This repo's
[`/submissions`](../submissions/) structure is set up to hold that round's deliverable
alongside this one without needing to restructure anything.
