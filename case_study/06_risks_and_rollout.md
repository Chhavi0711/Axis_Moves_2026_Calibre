# 06 - Risks and Rollout

## Risks we named up front, and why

We treated risk identification as part of the pitch itself, not an appendix - a jury
evaluating "Operating Model & Execution Feasibility" is implicitly asking "what breaks
this, and have you thought about it," so we built our three biggest risks into the
core proposal rather than waiting to be asked.

### Risk 1 - Gaming the system

**The concern:** if Calibre scores influence who gets matched to (and eventually,
implicitly, who looks good), employees have an incentive to cherry-pick easy, low-risk
cases to keep their score high, rather than take on harder judgment calls.

**Our mitigation:** difficulty-adjusted audits - the scoring mechanism doesn't just
count good outcomes, it weighs them against how hard the case was, and this weighting is
independently audited rather than self-reported or opaque. This is also why we scoped
governance/fairness auditing as a standing function in the operating model (see
[`04_operating_model.md`](04_operating_model.md)), not a one-time check at launch.

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

## What we intentionally left for later rounds

We did not attempt, in this round's 2-slide format, to fully specify:

- The exact audit methodology for difficulty-adjusted scoring
- A detailed data/privacy design for how Calibre records are stored, accessed, and
  governed internally
- A named pilot timeline or specific regions

These are natural candidates for Round 4's "Detailed PPT," once/if we have that
material - this repo's [`/submissions`](../submissions/) structure is set up to hold
that round's deliverable alongside this one without needing to restructure anything.
