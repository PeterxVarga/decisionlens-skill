# Changelog

## V1 Decision Qualification Engine — falsified / not released

- Built an isolated V1 candidate around decision-question locking, evidence/claim ceilings, directional discriminators, disconfirming evidence, minimum discriminating evidence, and downstream scope ceilings.
- Ran a frozen Wave 02 hostile evaluation: 8 cases, 6 primary lanes, plus 4 high-risk secondary challenges; 52 executions total.
- V1 produced 0 fatal failures and passed 7/8 targeted behaviors, but failed the frozen release gates.
- It materially beat the minimal prompt baseline on 3/8 cases (required 4/8) and LobeHub Product Design on 2/8 cases (required 3/8).
- Mandatory CASE-01 failed because the candidate still overclaimed an exact downstream administration placement after a correct upstream product-context conclusion.
- The candidate also triggered the ceremony-tax failure: more framework/output without enough material capability gain.
- Final verdict: **FAIL — KEEP V0**.
- The V1 candidate was not merged into the model-visible runtime.
- Recorded one surviving observation for real-product monitoring: downstream confidence should not automatically inherit upstream confidence.

See [`benchmark/WAVE02-V1-FALSIFICATION.md`](benchmark/WAVE02-V1-FALSIFICATION.md).

## V0 — Frozen public release

- Frozen Product Architecture Review runtime.
- Added public documentation and installation guidance.
- Added controlled Wave 01 benchmark evidence.
- Added five canonical examples.
- Added bounded public claims and launch copy.

No post-bake-off methodology changes were made to the model-visible runtime.
