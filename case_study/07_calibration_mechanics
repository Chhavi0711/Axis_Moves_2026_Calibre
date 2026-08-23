# 07 - Calibration Mechanics

*This doc goes deeper than the two-slide submission itself. It's built from the team's
own prep material ([`/docs/prep_materials`](../docs/prep_materials/)) - the answers we
worked out for the questions a sharp jury would actually press on, even though the
deck's 2-slide format couldn't carry this much density.*

## The Calibration Score, step by step

We call the underlying mechanic the **Calibration Score** - not a vague "good employee"
rating, but a specific, difficulty-adjusted comparison of predicted outcome versus
actual outcome, recalculated on a fixed schedule.

- Every discretionary decision (a sanctioning call, a pricing exception, a risk
  override) is logged with the case's difficulty tier **at the time it's decided**, not
  after the fact - so nobody can argue a case was harder than it looked once the outcome
  is known.
- Difficulty tiering uses objective, pre-set factors the Governance Committee owns:
  loan size relative to segment norms, sector volatility, borrower's documentation
  completeness, and whether the request falls outside standard policy. This produces a
  Low / Medium / High difficulty bucket for each case.
- Once the case resolves, the actual result is compared to what a well-calibrated
  decision in that difficulty tier should look like - scored **within the tier**, not
  against the whole portfolio, so someone handling harder cases isn't penalised for
  naturally higher variance.
- Scores are recency-weighted: a rolling window (modelled at 18-24 months, matching
  typical credit outcome visibility) weights recent decisions more heavily than older
  ones, so the score reflects current judgment, not a strong quarter from three years
  ago.
- A minimum sample size - 30 difficulty-adjusted cases, as a working threshold - is
  required before someone's authority moves meaningfully. Below that, they sit at a
  stable baseline tied to their existing grade, so one lucky or unlucky month can't swing
  their authority.
- Authority limits update on a **quarterly** cadence, signed off by the Governance
  Committee - not continuously in real time. AI can use live scores for case-routing
  (who's best suited right now), but actual discretionary limits only move after a
  human governance review, which keeps the system auditable and prevents whiplash.

## A concrete example

Say an SME credit officer handles 40 cases in a quarter - 12 Low, 20 Medium, 8 High
difficulty. Her High-tier cases have a slightly higher exception rate than average, but
that's expected and priced into the High-tier benchmark. Her Medium and Low-tier
calibration is strong. The blended, difficulty-adjusted score comes out well above her
segment's baseline. That moves her sanctioning limit up one band next quarter - not
because she made more decisions, but because the ones she made held up, adjusted for how
hard they were.

## Bootstrapping before enough data exists

Year one calibration starts from existing performance-review and audit data as a
baseline, recalibrated quarterly as real Calibre-based outcomes accumulate - so the
system doesn't have to wait years to produce a usable signal, but also doesn't
overclaim precision on day one.

## Does this apply the same way across functions?

The difficulty-tiering criteria and outcome-observation windows are function-specific -
credit outcomes take longer to observe than a pricing exception, for instance - but the
underlying logic (predicted vs. actual, difficulty-adjusted, recency-weighted) is the
same across domains. This is what makes the mechanism portable in the Enterprise stage
of the rollout (see [`06_risks_and_rollout.md`](06_risks_and_rollout.md)).

## What a downturn does to the score

Scores are relative within difficulty tier and time period, not against a fixed
historical bar. A system-wide downturn shifts the whole benchmark, so a well-calibrated
officer in a bad year still scores well relative to that year's conditions - nobody is
being asked to out-predict the economy.
